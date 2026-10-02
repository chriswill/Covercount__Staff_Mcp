# CoverCount Staff

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

**OpenAI review metadata (October 1, 2026):** version `1.2.8` names the product
**CoverCount Staff** and adds five positive
and three negative cases, the owner's demo recording, United States availability,
and the owner's no-purchases/payments declaration with an explicit explanation of
existing cancellation-refund recovery. The canonical fields are in root
`plugin.json` under `extensions.com.openai.review` and `publication`. OpenAI uses
these portable fields ahead of the Codex compatibility manifest; do not maintain
a second copy of the cases there. Reupload
`covercount-openai-new-listing-1.2.8.zip` to the **same `covercount-staff` draft**.
The builder also generates `covercount-openai-new-listing-1.2.8-review.md` outside
the ZIP with all metadata, fixture requirements and a recording walkthrough.
Cases are drafted, not run. Reviewer access and credentials belong in the secure
portal fields. MCP connection, live case execution and submission remain separate.

**OpenAI listing clarification (October 1, 2026):** version `1.2.7` selects
**Business & Operations**, states the restaurant/venue staff audience explicitly,
and uses concrete workflow labels in the listing. This responds to the portal's
category-fit warning on `1.2.6`. Reupload
`covercount-openai-new-listing-1.2.7.zip` to the **same `covercount-staff` draft**;
the `new-listing` build target means the replacement identity, including later
updates to it. No further listing or MCP connection change is needed for this
metadata patch. The portal subsequently showed **No Issues** for metadata and
**Checks passed** for all five skills. Review information and MCP setup were still
incomplete; `1.2.8` supplies the review metadata.

**Replacement identity introduced in 1.2.6 (October 1, 2026):** version `1.2.6` adds
the separate `openaiNewListing` export identity `covercount-staff` in
[distribution.json](distribution.json). Build with
`python resources/scripts/build-covercount-plugin.py --openai-target new-listing`
from the Reservations workspace. The resulting
`covercount-openai-new-listing-1.2.8.zip` targets the **replacement public listing**, with one
`covercount` MCP key and all five canonical skill names. Its endpoint, skills,
prompts and branding are unchanged. Connection setup, review materials, review
and publication must be completed for the new listing; existing user connections
are not migrated by this package. The legacy identity below remains recorded
separately. No new listing or unpublication has been performed by the builder.

**Legacy OpenAI update blocked (October 1, 2026):** the `1.2.4` draft passes metadata
and skill checks but lists an unresolved `covercount` declaration alongside the
authorized legacy **CoverCount Staff** connection. Removing that declaration in
candidate `1.2.5` was rejected by the portal as an unsupported MCP-server change.
Do not use `1.2.5` as a fix. The failed omission rule was withdrawn. Following
support guidance supplied by the owner, the replacement package uses a new
identity rather than attempting another change to that existing listing.
The last verified portal state was published `1.0.0` and saved draft `1.2.4`;
`1.2.5` was not accepted or published. Unpublishing changes public visibility;
it does not establish that the legacy identity can accept this replacement ZIP.

Version `1.2.4` adds the portable OpenAI `plugin.json` and `mcp.json`, restores
the support link, and fits the listing subtitle within 30 characters. The Staff
skills, prompts, icon and authenticated MCP endpoint are unchanged. The complete
`covercount-openai-1.2.4.zip` includes all five skills and the MCP declaration;
it is a saved draft with the unresolved setup issue above, not an approved update.
The package includes release notes; existing demo, reviewer access, countries
and publisher verification remain separate portal requirements.

The legacy OpenAI Staff listing requires the internal package name
`app-6aaac50b4e908191bd7d24e896d729bf`, confirmed by the portal's upload rejection
on October 1, 2026. [distribution.json](distribution.json) records that identity
for the release builder's explicit `--openai-target existing-listing` option.
That export uses it for both manifests and the
ZIP's root folder, while the visible product name is **CoverCount Staff**. The source and
combined Codex/Claude package retain `covercount`; the MCP connection key also
remains `covercount` at `https://mcp.covercount.io/mcp`. The portal's existing app
is `asdk_app_6aaac50b4e908191bd7d24e896d729bf`, shown as authorized and domain
verified, with MCP key "Not specified". Its downloaded published `1.0.0` ZIP has
no MCP/app configuration files. This evidence does not make removing the current
draft's declaration a supported update; the portal has explicitly rejected it.

OpenAI limits `plugin-name:skill-name` to 64 characters. Its export therefore
maps `covercount-manage-reservations` to `manage-reservations` and
`covercount-reservation-briefing` to `reservation-briefing`, including folder
names, frontmatter and explicit skill invocations. Other skill names and all
workflow instructions remain unchanged. These aliases apply only to the legacy
Staff export; the replacement `covercount-staff` export needs no aliases.
Do not copy either Staff identity to Explore.

Version `1.2.3` replaces the default listing icon with the supplied 1024 x 1024
PNG emblem at [assets/icon.png](assets/icon.png), including composer and light/dark
logo metadata. Use this PNG when a directory submission asks for an icon upload.
Anthropic previously set the Staff listing icon manually; the packaged asset does
not confirm that the hosted listing has refreshed.

Version `1.2.2` explains that approving an event change or refund recovery in
CoverCount also executes the reviewed request. Assistants read its status before
any recovery commit; no second chat confirmation is needed. This behavior requires
the corresponding API/ui update. It retains event-detail guidance from `1.2.1`
and email messaging from `1.2.0`; refresh MCP instructions and installed skills.
The directory includes portable OpenAI, Codex and Claude
Code manifests for the same remote MCP connection. Host-specific installation,
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
