# LaGrowthMachine: Native API Reference

A consolidated summary of LaGrowthMachine's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/2071164/TVCmSkH2
- **API base URL:** `https://apiv2.lagrowthmachine.com/flow`

## Authentication

### API Key

Connect LaGrowthMachine with an API key generated from your account settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://documenter.getpostman.com/view/2071164/TVCmSkH2)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Audience from LinkedIn URL](actions/create-audience-from-linked-in-url.md) | `POST /audiences` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [Create Inbox Webhook](actions/create-inbox-webhook.md) | `POST /inboxWebhooks` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [Create or Update Lead](actions/create-or-update-lead.md) | `POST /leads` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [Delete Inbox Webhook](actions/delete-inbox-webhook.md) | `DELETE /inboxWebhooks/:webhookId` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [Edit Inbox Conversation Note](actions/edit-inbox-conversation-note.md) | `POST /inbox/conversations/note` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:campaignId` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [Get Campaign Lead Stats](actions/get-campaign-lead-stats.md) | `GET /campaigns/:campaignId/statsleads` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [Get Campaign Stats](actions/get-campaign-stats.md) | `GET /campaigns/:campaignId/stats` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [List Audiences](actions/list-audiences.md) | `GET /audiences` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [List Identities](actions/list-identities.md) | `GET /identities` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [List Inbox Webhooks](actions/list-inbox-webhooks.md) | `GET /inboxWebhooks` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [List Members](actions/list-members.md) | `GET /members` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [Remove Lead from Audiences](actions/remove-lead-from-audiences.md) | `POST /leads/removefromaudience` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [Search Leads](actions/search-leads.md) | `GET /leads/search` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [Send Email Message](actions/send-email-message.md) | `POST /inbox/email` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [Send LinkedIn Message](actions/send-linked-in-message.md) | `POST /inbox/linkedin` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
| [Update Lead Status](actions/update-lead-status.md) | `POST /leads/status` | [docs](https://documenter.getpostman.com/view/2071164/TVCmSkH2) |
