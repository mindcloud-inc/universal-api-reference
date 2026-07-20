# HelpDesk: Native API Reference

A consolidated summary of HelpDesk's API configuration and 52 documented operations, with links to official documentation.

- **Official docs:** https://api.helpdesk.com/docs
- **API base URL:** `https://api.helpdesk.com`

## Authentication

### Account ID + PAT

Connect HelpDesk with your account ID as the username and a Personal Access Token as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://api.helpdesk.com/docs#section/Authentication)

## Pagination

Use `pageSize` in the query string to set the page size (default 20; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (52 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Agent](actions/get-agent.md) | `GET /v1/agents/:agentID` | [docs](https://api.helpdesk.com/docs#tag/Agents/operation/agentsRead) |
| [Get Blocked Email](actions/get-blocked-email.md) | `GET /v1/blockedEmails/:blockedEmailID` | [docs](https://api.helpdesk.com/docs#tag/Spam-management/operation/blockedEmailsRead) |
| [Get Canned Response](actions/get-canned-response.md) | `GET /v1/cannedResponses/:cannedResponseID` | [docs](https://api.helpdesk.com/docs#tag/Canned-responses/operation/cannedResponsesRead) |
| [Get Custom Field](actions/get-custom-field.md) | `GET /v1/customFields/:customFieldID` | [docs](https://api.helpdesk.com/docs#tag/Custom-fields/operation/customFieldsRead) |
| [Get Email Domain](actions/get-email-domain.md) | `GET /v1/emailDomains/:domainID` | [docs](https://api.helpdesk.com/docs#tag/Email-domains/operation/emailDomainRead) |
| [Get Failed Outgoing Emails Report](actions/get-failed-outgoing-emails-report.md) | `GET /v1/reports/failedEmails` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportFailedEmails) |
| [Get License](actions/get-license.md) | `GET /v1/licenses/:licenseID` | [docs](https://api.helpdesk.com/docs#tag/Licenses/operation/licensesRead) |
| [Get Macro](actions/get-macro.md) | `GET /v1/macros/:macroID` | [docs](https://api.helpdesk.com/docs#tag/Macros/operation/macroRead) |
| [Get Mailbox](actions/get-mailbox.md) | `GET /v1/mailboxes/:mailboxID` | [docs](https://api.helpdesk.com/docs#tag/Mailboxes-(inboxes)/operation/mailboxRead) |
| [Get New Tickets Report](actions/get-new-tickets-report.md) | `GET /v1/reports/newTickets` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportNewTickets) |
| [Get New Tickets 24h Distribution Report](actions/get-new-tickets24h-distribution-report.md) | `GET /v1/reports/newTickets24` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportNewTickets24) |
| [Get Reply Address](actions/get-reply-address.md) | `GET /v1/replyAddresses/:replyAddressID` | [docs](https://api.helpdesk.com/docs#tag/Reply-addresses/operation/replyAddressRead) |
| [Get Resolution Time Per Agent Report](actions/get-resolution-time-per-agent-report.md) | `GET /v1/reports/resolutionTimePerAgent` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportResolutionTimePerAgent) |
| [Get Resolution Time Per Team Report](actions/get-resolution-time-per-team-report.md) | `GET /v1/reports/resolutionTimePerTeam` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportResolutionTimePerTeam) |
| [Get Resolution Time Report](actions/get-resolution-time-report.md) | `GET /v1/reports/resolutionTime` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportResolutionTime) |
| [Get Resolution Time 24h Distribution Report](actions/get-resolution-time24h-distribution-report.md) | `GET /v1/reports/resolutionTime24` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportResolutionTime24) |
| [Get Response Time Per Agent Report](actions/get-response-time-per-agent-report.md) | `GET /v1/reports/responseTimePerAgent` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportResponseTimePerAgent) |
| [Get Response Time Per Team Report](actions/get-response-time-per-team-report.md) | `GET /v1/reports/responseTimePerTeam` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportResponseTimePerTeam) |
| [Get Response Time Report](actions/get-response-time-report.md) | `GET /v1/reports/responseTime` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportResponseTime) |
| [Get Response Time 24h Distribution Report](actions/get-response-time24h-distribution-report.md) | `GET /v1/reports/responseTime24` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportResponseTime24) |
| [Get Rule](actions/get-rule.md) | `GET /v1/rules/:ruleID` | [docs](https://api.helpdesk.com/docs#tag/Rules/operation/ruleRead) |
| [Get Tag](actions/get-tag.md) | `GET /v1/tags/:tagID` | [docs](https://api.helpdesk.com/docs#tag/Tags/operation/tagRead) |
| [Get Team](actions/get-team.md) | `GET /v1/teams/:teamID` | [docs](https://api.helpdesk.com/docs#tag/Teams/operation/teamRead) |
| [Get Template](actions/get-template.md) | `GET /v1/templates/:templateID` | [docs](https://api.helpdesk.com/docs#tag/Templates/operation/templateRead) |
| [Get Ticket](actions/get-ticket.md) | `GET /v1/tickets/:ticketID` | [docs](https://api.helpdesk.com/docs#tag/Tickets/operation/ticketRead) |
| [Get Ticket Rating Report](actions/get-ticket-rating-report.md) | `GET /v1/reports/rating` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportRating) |
| [Get Ticket Rating 24h Distribution Report](actions/get-ticket-rating24h-distribution-report.md) | `GET /v1/reports/rating24` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportRating24) |
| [Get Ticket Sources 24h Distribution Report](actions/get-ticket-sources24h-distribution-report.md) | `GET /v1/reports/ticketSources24` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportTicketSources24) |
| [Get Ticket Status Report](actions/get-ticket-status-report.md) | `GET /v1/reports/status` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportStatus) |
| [Get Ticket Status 24h Distribution Report](actions/get-ticket-status24h-distribution-report.md) | `GET /v1/reports/status24` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportStatus24) |
| [Get Tickets Status Per Agent Report](actions/get-tickets-status-per-agent-report.md) | `GET /v1/reports/statusPerAgent` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportStatusPerAgent) |
| [Get Tickets Status Per Team Report](actions/get-tickets-status-per-team-report.md) | `GET /v1/reports/statusPerTeam` | [docs](https://api.helpdesk.com/docs#tag/Reports/operation/reportStatusPerTeam) |
| [Get Trusted Email](actions/get-trusted-email.md) | `GET /v1/trustedEmails/:trustedEmailID` | [docs](https://api.helpdesk.com/docs#tag/Spam-management/operation/treustedEmailRead) |
| [Get View](actions/get-view.md) | `GET /v1/views/:viewID` | [docs](https://api.helpdesk.com/docs#tag/Views/operation/viewRead) |
| [List Agents](actions/list-agents.md) | `GET /v1/agents` | [docs](https://api.helpdesk.com/docs#tag/Agents/operation/agentsList) |
| [List Audit Log](actions/list-audit-log.md) | `GET /v1/auditLog` | [docs](https://api.helpdesk.com/docs#tag/Audit-log/operation/auditLog) |
| [List Blocked Emails](actions/list-blocked-emails.md) | `GET /v1/blockedEmails` | [docs](https://api.helpdesk.com/docs#tag/Spam-management/operation/blockedEmailsList) |
| [List Canned Responses](actions/list-canned-responses.md) | `GET /v1/cannedResponses` | [docs](https://api.helpdesk.com/docs#tag/Canned-responses/operation/cannedResponsesList) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /v1/customFields` | [docs](https://api.helpdesk.com/docs#tag/Custom-fields/operation/customFieldsList) |
| [List Email Domains](actions/list-email-domains.md) | `GET /v1/emailDomains` | [docs](https://api.helpdesk.com/docs#tag/Email-domains/operation/emailDomainsList) |
| [List Licenses](actions/list-licenses.md) | `GET /v1/licenses` | [docs](https://api.helpdesk.com/docs#tag/Licenses/operation/licensesList) |
| [List Macros](actions/list-macros.md) | `GET /v1/macros` | [docs](https://api.helpdesk.com/docs#tag/Macros/operation/macrosList) |
| [List Mailboxes](actions/list-mailboxes.md) | `GET /v1/mailboxes` | [docs](https://api.helpdesk.com/docs#tag/Mailboxes-(inboxes)/operation/mailboxesList) |
| [List Reply Addresses](actions/list-reply-addresses.md) | `GET /v1/replyAddresses` | [docs](https://api.helpdesk.com/docs#tag/Reply-addresses/operation/replyAddressesList) |
| [List Rules](actions/list-rules.md) | `GET /v1/rules` | [docs](https://api.helpdesk.com/docs#tag/Rules/operation/rulesList) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /v1/subscriptions` | [docs](https://api.helpdesk.com/docs#tag/Subscriptions/operation/subscriptionsList) |
| [List Tags](actions/list-tags.md) | `GET /v1/tags` | [docs](https://api.helpdesk.com/docs#tag/Tags/operation/tagsList) |
| [List Teams](actions/list-teams.md) | `GET /v1/teams` | [docs](https://api.helpdesk.com/docs#tag/Teams/operation/teamsList) |
| [List Templates](actions/list-templates.md) | `GET /v1/templates` | [docs](https://api.helpdesk.com/docs#tag/Templates/operation/templatesList) |
| [List Tickets](actions/list-tickets.md) | `GET /v1/tickets` | [docs](https://api.helpdesk.com/docs#tag/Tickets/operation/ticketList) |
| [List Trusted Emails](actions/list-trusted-emails.md) | `GET /v1/trustedEmails` | [docs](https://api.helpdesk.com/docs#tag/Spam-management/operation/trustedList) |
| [List Views](actions/list-views.md) | `GET /v1/views` | [docs](https://api.helpdesk.com/docs#tag/Views/operation/viewsList) |
