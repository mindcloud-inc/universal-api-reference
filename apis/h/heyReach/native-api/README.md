# Hey Reach: Native API Reference

A consolidated summary of Hey Reach's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/23808049/2sA2xb5F75
- **API base URL:** `https://api.heyreach.io`

## Authentication

### API Key

Use a HeyReach Public API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://documenter.getpostman.com/view/23808049/2sA2xb5F75#ac5dd276-52d6-4cf2-a0ce-bd21d8766a7c)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `text/plain` |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the request body to set the page size (default 100; maximum 100). Use `offset` in the request body as the record offset; numbering starts at 0.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Lead Tags](actions/add-lead-tags.md) | `POST /api/public/lead/AddTags` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Add Leads To Campaign](actions/add-leads-to-campaign.md) | `POST /api/public/campaign/AddLeadsToCampaignV2` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Add Leads To List](actions/add-leads-to-list.md) | `POST /api/public/list/AddLeadsToListV2` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Create Empty List](actions/create-empty-list.md) | `POST /api/public/list/CreateEmptyList` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Create Lead Tags](actions/create-lead-tags.md) | `POST /api/public/lead_tags/CreateTags` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/public/webhooks/CreateWebhook` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /api/public/webhooks/DeleteWebhook` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Get Campaign](actions/get-campaign.md) | `GET /api/public/campaign/GetById` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Get Conversation](actions/get-conversation.md) | `GET /api/public/inbox/GetChatroom/:accountId/:conversationId` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Get Lead](actions/get-lead.md) | `POST /api/public/lead/GetLead` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Get Lead Tags](actions/get-lead-tags.md) | `POST /api/public/lead/GetTags` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Get List](actions/get-list.md) | `GET /api/public/list/GetById` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Get Overall Stats](actions/get-overall-stats.md) | `POST /api/public/stats/GetOverallStats` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Get Webhook](actions/get-webhook.md) | `GET /api/public/webhooks/GetWebhookById` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [List Campaign Leads](actions/list-campaign-leads.md) | `POST /api/public/campaign/GetLeadsFromCampaign` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [List Campaigns](actions/list-campaigns.md) | `POST /api/public/campaign/GetAll` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [List Campaigns For Lead](actions/list-campaigns-for-lead.md) | `POST /api/public/campaign/GetCampaignsForLead` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [List Companies In List](actions/list-companies-in-list.md) | `POST /api/public/list/GetCompaniesFromList` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [List Conversations](actions/list-conversations.md) | `POST /api/public/inbox/GetConversationsV2` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [List Leads In List](actions/list-leads-in-list.md) | `POST /api/public/list/GetLeadsFromList` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [List LinkedIn Accounts](actions/list-linked-in-accounts.md) | `POST /api/public/li_account/GetAll` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [List Lists](actions/list-lists.md) | `POST /api/public/list/GetAll` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [List Lists For Lead](actions/list-lists-for-lead.md) | `POST /api/public/list/GetListsForLead` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [List Webhooks](actions/list-webhooks.md) | `POST /api/public/webhooks/GetAllWebhooks` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Pause Campaign](actions/pause-campaign.md) | `POST /api/public/campaign/Pause` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Replace Lead Tags](actions/replace-lead-tags.md) | `POST /api/public/lead/ReplaceTags` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Resume Campaign](actions/resume-campaign.md) | `POST /api/public/campaign/Resume` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Send Message](actions/send-message.md) | `POST /api/public/inbox/SendMessage` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Stop Lead In Campaign](actions/stop-lead-in-campaign.md) | `POST /api/public/campaign/StopLeadInCampaign` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /api/public/webhooks/UpdateWebhook` | [docs](https://documenter.getpostman.com/view/23808049/2sA2xb5F75) |
