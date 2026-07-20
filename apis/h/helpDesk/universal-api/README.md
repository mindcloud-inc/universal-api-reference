# <img src="https://images.mindcloud.co/apps/icons/helpdesk-icon-filled-256_1774639525407.png" alt="HelpDesk logo" width="28" height="28"> HelpDesk: Universal API

Manage tickets, teams, tags, and helpdesk workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/helpDesk/latest
- **Category:** Support / Ticketing
- **Actions:** 52
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.helpdesk.com
- **Vendor API docs:** https://api.helpdesk.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tickets](actions/list-tickets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (52)

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get License](actions/get-license.md) | GET | Retrieves a license from HelpDesk. |
| [List Licenses](actions/list-licenses.md) | GET | Retrieves licenses from HelpDesk. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Get Blocked Email](actions/get-blocked-email.md) | GET | Retrieves a blocked email from HelpDesk. |
| [Get Canned Response](actions/get-canned-response.md) | GET | Retrieves a canned response from HelpDesk. |
| [Get Custom Field](actions/get-custom-field.md) | GET | Retrieves a custom field from HelpDesk. |
| [Get Email Domain](actions/get-email-domain.md) | GET | Retrieves an email domain from HelpDesk. |
| [Get Failed Outgoing Emails Report](actions/get-failed-outgoing-emails-report.md) | GET | Retrieves the failed outgoing emails report from HelpDesk. |
| [Get Macro](actions/get-macro.md) | GET | Retrieves a macro from HelpDesk. |
| [Get Mailbox](actions/get-mailbox.md) | GET | Retrieves a mailbox from HelpDesk. |
| [Get New Tickets Report](actions/get-new-tickets-report.md) | GET | Retrieves the new tickets report from HelpDesk. |
| [Get New Tickets 24h Distribution Report](actions/get-new-tickets24h-distribution-report.md) | GET | Retrieves the 24-hour new tickets distribution from HelpDesk. |
| [Get Reply Address](actions/get-reply-address.md) | GET | Retrieves a reply address from HelpDesk. |
| [Get Resolution Time Per Agent Report](actions/get-resolution-time-per-agent-report.md) | GET | Retrieves the resolution time per agent report from HelpDesk. |
| [Get Resolution Time Per Team Report](actions/get-resolution-time-per-team-report.md) | GET | Retrieves the resolution time per team report from HelpDesk. |
| [Get Resolution Time Report](actions/get-resolution-time-report.md) | GET | Retrieves the resolution time report from HelpDesk. |
| [Get Resolution Time 24h Distribution Report](actions/get-resolution-time24h-distribution-report.md) | GET | Retrieves the 24-hour resolution time distribution from HelpDesk. |
| [Get Response Time Per Agent Report](actions/get-response-time-per-agent-report.md) | GET | Retrieves the response time per agent report from HelpDesk. |
| [Get Response Time Per Team Report](actions/get-response-time-per-team-report.md) | GET | Retrieves the response time per team report from HelpDesk. |
| [Get Response Time Report](actions/get-response-time-report.md) | GET | Retrieves the response time report from HelpDesk. |
| [Get Response Time 24h Distribution Report](actions/get-response-time24h-distribution-report.md) | GET | Retrieves the 24-hour response time distribution from HelpDesk. |
| [Get Rule](actions/get-rule.md) | GET | Retrieves a rule from HelpDesk. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from HelpDesk. |
| [Get Ticket Rating Report](actions/get-ticket-rating-report.md) | GET | Retrieves the ticket rating report from HelpDesk. |
| [Get Ticket Rating 24h Distribution Report](actions/get-ticket-rating24h-distribution-report.md) | GET | Retrieves the 24-hour ticket rating distribution from HelpDesk. |
| [Get Ticket Sources 24h Distribution Report](actions/get-ticket-sources24h-distribution-report.md) | GET | Retrieves the 24-hour ticket sources distribution from HelpDesk. |
| [Get Ticket Status Report](actions/get-ticket-status-report.md) | GET | Retrieves the ticket status report from HelpDesk. |
| [Get Ticket Status 24h Distribution Report](actions/get-ticket-status24h-distribution-report.md) | GET | Retrieves the 24-hour ticket status distribution from HelpDesk. |
| [Get Tickets Status Per Agent Report](actions/get-tickets-status-per-agent-report.md) | GET | Retrieves the ticket status per agent report from HelpDesk. |
| [Get Tickets Status Per Team Report](actions/get-tickets-status-per-team-report.md) | GET | Retrieves the ticket status per team report from HelpDesk. |
| [Get Trusted Email](actions/get-trusted-email.md) | GET | Retrieves a trusted email from HelpDesk. |
| [Get View](actions/get-view.md) | GET | Retrieves a view from HelpDesk. |
| [List Audit Log](actions/list-audit-log.md) | GET | Retrieves audit log events from HelpDesk. |
| [List Blocked Emails](actions/list-blocked-emails.md) | GET | Retrieves blocked emails from HelpDesk. |
| [List Canned Responses](actions/list-canned-responses.md) | GET | Retrieves canned responses from HelpDesk. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from HelpDesk. |
| [List Email Domains](actions/list-email-domains.md) | GET | Retrieves email domains from HelpDesk. |
| [List Macros](actions/list-macros.md) | GET | Retrieves macros from HelpDesk. |
| [List Mailboxes](actions/list-mailboxes.md) | GET | Retrieves mailboxes from HelpDesk. |
| [List Reply Addresses](actions/list-reply-addresses.md) | GET | Retrieves reply addresses from HelpDesk. |
| [List Rules](actions/list-rules.md) | GET | Retrieves rules from HelpDesk. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from HelpDesk. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from HelpDesk. |
| [List Trusted Emails](actions/list-trusted-emails.md) | GET | Retrieves trusted emails from HelpDesk. |
| [List Views](actions/list-views.md) | GET | Retrieves views from HelpDesk. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from HelpDesk. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from HelpDesk. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from HelpDesk. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from HelpDesk. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from HelpDesk. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves a ticket from HelpDesk. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent](actions/get-agent.md) | GET | Retrieves an agent from HelpDesk. |
| [List Agents](actions/list-agents.md) | GET | Retrieves agents from HelpDesk. |

