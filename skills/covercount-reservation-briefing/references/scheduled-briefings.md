# Scheduled briefing runs

Use the task's configured venue connection, period, service window and output
destination. Scheduling and delivery belong to the calling client, not to the
CoverCount summary tool. Do not claim a task was scheduled or delivered without
evidence from that client. Creating or modifying a schedule is a separate user
request and depends on the client's available scheduling capability.

For daily and weekly runs, prefer the reusable `today`, `tomorrow`, `next_7_days`
or `next_week` argument. Never retain dates from a sample or previous execution.
The response's resolved dates and timezone determine the report heading.

For a configured evening window, obtain the current venue-local date from a
trusted current clock and the venue timezone. If that context is unavailable,
`summarize_reservations` with `period: "today"` supplies today's local bounds;
use those bounds only to resolve the configured evening's custom interval, then
make a fresh custom summary read. A midnight or earlier ending clock time belongs
to the following date for an explicitly configured overnight service window.

If "tonight" has no configured service hours and no person is available to answer,
return a short configuration-needed result rather than guessing. If authentication
expires or is revoked, report that fresh data is unavailable and that the
connection needs attention. Do not reuse yesterday's report as today's or route
around authorization with a different account.

Stop after a successful read and briefing. For a transient read failure, one
retry is reasonable; persistent failure should produce a brief unavailable result.
Do not repeatedly poll, modify reservations, or send SMS while generating a report.

Example reusable task text:

> Use $covercount-reservation-briefing to read today's CoverCount reservations.
> Give the venue, local date and as-of time; reservation and cover totals; largest
> parties and times; and recorded birthday/anniversary highlights with coverage.
> If the read fails, say the briefing could not be refreshed.

For a weekly task, substitute "next calendar week, Monday through Sunday" and ask
for a daily table. Verify actual recurring tool access, date rollover, refresh,
and failure reporting in the chosen scheduling client before relying on it.
