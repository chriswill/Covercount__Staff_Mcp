# CoverCount

Get reservation and event briefings and manage operations for your connected
CoverCount venue. Sign in with your own CoverCount staff account and approve the
access you want the assistant to have.

Try:

- "What do my reservations look like next week?"
- "How are this week's events doing?"
- "Help me find and update a reservation."
- "Which table is this reservation on? Move it to table 12."
- "Draft an email to the guest about their reservation."

The five included skills cover reservation briefings, reservation management,
individual guest messages, event operations and recovery of an existing
cancellation refund. Briefings report current recorded facts and their time
period. Event financials require additional consent and a manager or admin role.

For "tonight", provide the venue's evening service window once so the briefing
uses the intended hours. A scheduled briefing also needs a client that supports
scheduling and a continuing authorized connection; this plugin does not create a
schedule by itself.

Reservation creation, cancellation and modification run when you request them
and the required details are clear. For a message the assistant drafts or edits,
it shows the exact text, booking, channel, recipient and email subject for your
confirmation before sending. An
explicit request to send your own exact text can proceed directly.

Event publication, capacity changes and cancellation refund recovery still require
your review in CoverCount. Messages and refunds can remain pending after an
operation succeeds; the assistant checks status instead of repeating the action.

Guest messages support email and SMS. When you leave the channel open, the
assistant prefers eligible email. Email requires separate consent and works
without SMS setup or opt-in. An explicit request to text will not silently become
email. Email uses the configured sender; CoverCount does not provide a reply inbox.

Version `1.2.1` adds event-detail guidance for ticket prices, capacity, paid/free/
complimentary counts and venue-local sales cutoffs. It retains email messaging
and channel eligibility from `1.2.0`. The event overview requires the corresponding
MCP server update and refreshed tool discovery. The directory includes Codex and Claude
Code manifests with one shared remote MCP connection. Host-specific installation,
OAuth and skill activation still need acceptance in the intended client.

## Privacy Policy

CoverCount's privacy policy is published at
<https://www.covercount.io/privacy>.

This plugin connects to the remote CoverCount MCP server at
`https://mcp.covercount.io/mcp` using your own CoverCount staff account. It
stores no data locally. Reservation, guest, event and messaging data accessed
through the connection is handled under the policy above, which covers what is
collected, how it is used and stored, the processors it is shared with, how long
it is retained, and how to exercise your rights.

Privacy questions: privacy@covercount.io

## License

Licensed under the Apache License, Version 2.0. See [LICENSE.txt](LICENSE.txt).

The license covers the plugin manifests, skills and documentation in this
repository. It does not grant rights to the CoverCount name, logos or other
brand assets, including the files in `assets/` (Apache License, Section 6).

[CoverCount](https://www.covercount.io/) ·
[Support](https://support.cloudscope.io/) ·
[Privacy](https://www.covercount.io/privacy) ·
[Terms](https://www.covercount.io/terms-of-service)
