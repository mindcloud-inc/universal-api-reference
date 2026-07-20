# LinkedCamp: Native API Reference

A consolidated summary of LinkedCamp's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://api.linkedcamp.com/docs/
- **API base URL:** `https://api.linkedcamp.com`

## Authentication

### API Key

Use a LinkedCamp API key. LinkedCamp expects it in the token request header.

### Credentials

- **API Key:** `apiKey` · required · LinkedCamp API key. Runtime requests send this value in the token header.

Send these headers with each API request:

```http
token: <apiKey>
```

[Official authentication documentation](https://help.linkedcamp.com/en/collections/11110389-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Blacklist Entry](actions/add-blacklist-entry.md) | `POST /blacklists` | [docs](https://api.linkedcamp.com/docs/) |
| [Add Leads To Campaign](actions/add-leads-to-campaign.md) | `POST /leads/add-to-campaign` | [docs](https://api.linkedcamp.com/docs/) |
| [Cancel Sub-Account](actions/cancel-sub-account.md) | `POST /users/cancel` | [docs](https://api.linkedcamp.com/docs/) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaigns/` | [docs](https://api.linkedcamp.com/docs/) |
| [Create Connect Campaign](actions/create-connect-campaign.md) | `POST /campaigns` | [docs](https://help.linkedcamp.com/en/articles/10257445-api-create-a-new-campaign) |
| [Create Email Campaign](actions/create-email-campaign.md) | `POST /campaigns` | [docs](https://help.linkedcamp.com/en/articles/10257445-api-create-a-new-campaign) |
| [Create InMail Campaign](actions/create-inmail-campaign.md) | `POST /campaigns` | [docs](https://help.linkedcamp.com/en/articles/10257445-api-create-a-new-campaign) |
| [Create Message Campaign](actions/create-message-campaign.md) | `POST /campaigns` | [docs](https://help.linkedcamp.com/en/articles/10257445-api-create-a-new-campaign) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://api.linkedcamp.com/docs/) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://api.linkedcamp.com/docs/) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhookId` | [docs](https://api.linkedcamp.com/docs/) |
| [Get Account API Token](actions/get-account-api-token.md) | `GET /tokens` | [docs](https://api.linkedcamp.com/docs/) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:campaignId` | [docs](https://api.linkedcamp.com/docs/) |
| [Get Campaign Stats](actions/get-campaign-stats.md) | `GET /campaigns/:campaignId/stats` | [docs](https://api.linkedcamp.com/docs/) |
| [Get Conversation Messages](actions/get-conversation-messages.md) | `GET /conversations/:conversationId` | [docs](https://api.linkedcamp.com/docs/) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://api.linkedcamp.com/docs/) |
| [Get Lead](actions/get-lead.md) | `GET /leads/:leadId` | [docs](https://api.linkedcamp.com/docs/) |
| [Get User Token](actions/get-user-token.md) | `GET /users/:userId` | [docs](https://api.linkedcamp.com/docs/) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:webhookId` | [docs](https://api.linkedcamp.com/docs/) |
| [List Blacklist Entries](actions/list-blacklist-entries.md) | `GET /blacklists` | [docs](https://api.linkedcamp.com/docs/) |
| [List Campaign Leads](actions/list-campaign-leads.md) | `GET /leads/` | [docs](https://api.linkedcamp.com/docs/) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns/` | [docs](https://api.linkedcamp.com/docs/) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://api.linkedcamp.com/docs/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://api.linkedcamp.com/docs/) |
| [Pause Sub-Account](actions/pause-sub-account.md) | `POST /users/pause` | [docs](https://api.linkedcamp.com/docs/) |
| [Register Sub-Account](actions/register-sub-account.md) | `POST /users/register` | [docs](https://api.linkedcamp.com/docs/) |
| [Resume Sub-Account](actions/resume-sub-account.md) | `POST /users/resume` | [docs](https://api.linkedcamp.com/docs/) |
| [Send Conversation Message](actions/send-conversation-message.md) | `POST /conversations/send-message` | [docs](https://api.linkedcamp.com/docs/) |
| [Update Campaign Status](actions/update-campaign-status.md) | `PUT /campaigns/:campaignId` | [docs](https://api.linkedcamp.com/docs/) |
| [Update Lead](actions/update-lead.md) | `POST /leads/update` | [docs](https://api.linkedcamp.com/docs/) |
| [Update Lead Campaign Status](actions/update-lead-campaign-status.md) | `PUT /leads/:leadId` | [docs](https://api.linkedcamp.com/docs/) |
