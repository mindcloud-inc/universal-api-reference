# Wrangle: Native API Reference

A consolidated summary of Wrangle's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://wrangle.apidocumentation.com/reference
- **API base URL:** `https://slack.wrangle.io/api/v1`

## Authentication

### API Key

Use a Wrangle API token with Slack workspace and user IDs.

### Credentials

- **API Key:** `apiKey` · required
- **Slack Workspace ID:** `slackWorkspaceId` · required · The Slack workspace ID shown on Wrangle's API & Integrations page.
- **Slack User ID:** `slackUserId` · required · The Slack user ID shown on Wrangle's API & Integrations page.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.wrangle.io/integrations/wrangle-api)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | `POST /tickets` | [docs](https://wrangle.apidocumentation.com/reference) |
| [Delete Ticket](actions/delete-ticket.md) | `DELETE /tickets/:ticketId` | [docs](https://wrangle.apidocumentation.com/reference) |
| [Get Inbox](actions/get-inbox.md) | `GET /inboxes/:inboxId` | [docs](https://wrangle.apidocumentation.com/reference) |
| [Get Inboxes](actions/get-inboxes.md) | `GET /inboxes` | [docs](https://wrangle.apidocumentation.com/reference) |
| [Get Ticket](actions/get-ticket.md) | `GET /tickets/:ticketId` | [docs](https://wrangle.apidocumentation.com/reference) |
| [Get Tickets](actions/get-tickets.md) | `GET /inboxes/:inboxId/tickets` | [docs](https://wrangle.apidocumentation.com/reference) |
| [Get Workflow](actions/get-workflow.md) | `GET /workflows/:workflowId` | [docs](https://wrangle.apidocumentation.com/reference) |
| [Get Workflows](actions/get-workflows.md) | `GET /workflows` | [docs](https://wrangle.apidocumentation.com/reference) |
| [Start Workflow](actions/start-workflow.md) | `POST /workflows/:workflowId/instances` | [docs](https://wrangle.apidocumentation.com/reference) |
| [Update Inbox](actions/update-inbox.md) | `PUT /inboxes/:inboxId` | [docs](https://wrangle.apidocumentation.com/reference) |
| [Update Ticket](actions/update-ticket.md) | `PUT /tickets/:ticketId` | [docs](https://wrangle.apidocumentation.com/reference) |
