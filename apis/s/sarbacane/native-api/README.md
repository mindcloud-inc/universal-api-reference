# Sarbacane: Native API Reference

A consolidated summary of Sarbacane's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://developers.sarbacane.com/
- **API base URL:** `https://api.sarbacane.com/v1`

## Authentication

### API Key + Account ID

Authenticate with your Sarbacane API key and account ID sent as request headers.

### Credentials

- **API Key:** `apiKey` · required · Your Sarbacane API key. This is sent as the `apiKey` header on every request.
- **Account ID:** `accountId` · required · Your Sarbacane account ID. This is sent as the `accountId` header on every request.

Send these headers with each API request:

```http
apiKey: <apiKey>
accountId: <accountId>
```

[Official authentication documentation](https://developers.sarbacane.com/authentification/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 300 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Campaign Blacklists](actions/add-campaign-blacklists.md) | `POST /campaigns/{campaignId}/blacklists` | [docs](https://developers.sarbacane.com/campaigns/#add-campaigns-blacklist) |
| [Add Campaign Content](actions/add-campaign-content.md) | `POST /campaigns/{campaignId}/content` | [docs](https://developers.sarbacane.com/campaigns/#import-template) |
| [Add Contact](actions/add-contact.md) | `POST /lists/{listId}/contacts` | [docs](https://developers.sarbacane.com/contacts/#add-a-contact) |
| [Add Webhook](actions/add-webhook.md) | `POST /webhooks` | [docs](https://developers.sarbacane.com/contacts/#add-a-webhook) |
| [Cancel Campaign](actions/cancel-campaign.md) | `POST /campaigns/{campaignId}/cancel` | [docs](https://developers.sarbacane.com/campaigns/#cancel-campaign) |
| [Create Email Campaign](actions/create-email-campaign.md) | `POST /campaigns/email` | [docs](https://developers.sarbacane.com/campaigns/#create-an-email-campaign) |
| [Create List](actions/create-list.md) | `POST /lists` | [docs](https://developers.sarbacane.com/contacts/#add-a-list) |
| [Create SMS Campaign](actions/create-sms-campaign.md) | `POST /campaigns/sms` | [docs](https://developers.sarbacane.com/campaigns/#create-a-sms-campaign) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /campaigns/{campaignId}` | [docs](https://developers.sarbacane.com/campaigns/#delete-campaign) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /lists/{listId}/contacts` | [docs](https://developers.sarbacane.com/contacts/#delete-a-contact) |
| [Delete List](actions/delete-list.md) | `DELETE /lists/{listId}` | [docs](https://developers.sarbacane.com/contacts/#delete-a-list) |
| [Empty List](actions/empty-list.md) | `POST /lists/{listId}/empty` | [docs](https://developers.sarbacane.com/contacts/#empty-a-list) |
| [Get Campaign Details](actions/get-campaign-details.md) | `GET /campaigns/{campaignId}` | [docs](https://developers.sarbacane.com/campaigns/#get-campaign-details) |
| [Get Campaign Statistics](actions/get-campaign-statistics.md) | `GET /reports/{campaignId}` | [docs](https://developers.sarbacane.com/campaigns/#get-campaign-statistics) |
| [Get Credits](actions/get-credits.md) | `GET /credits` | [docs](https://developers.sarbacane.com/account/#get-credits) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/{webhookId}` | [docs](https://developers.sarbacane.com/contacts/#get-webhook) |
| [Import Campaign List](actions/import-campaign-list.md) | `POST /campaigns/{campaignId}/list` | [docs](https://developers.sarbacane.com/campaigns/#import-list) |
| [Import Campaign Recipients](actions/import-campaign-recipients.md) | `POST /campaigns/{campaignId}/recipients` | [docs](https://developers.sarbacane.com/campaigns/#import-recipients) |
| [Import Campaign Template](actions/import-campaign-template.md) | `POST /campaigns/{campaignId}/send/{sendId}/content` | [docs](https://developers.sarbacane.com/campaigns/#add-content) |
| [Import Contacts](actions/import-contacts.md) | `POST /lists/{listId}/contacts/import` | [docs](https://developers.sarbacane.com/contacts/#add-a-block-of-contacts-json) |
| [List Campaign Recipients](actions/list-campaign-recipients.md) | `GET /campaigns/{campaignId}/recipients` | [docs](https://developers.sarbacane.com/campaigns/#list-recipients-campaign) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://developers.sarbacane.com/campaigns/#list-campaigns) |
| [List Contacts](actions/list-contacts.md) | `GET /lists/{listId}/contacts` | [docs](https://developers.sarbacane.com/contacts/#list-contacts) |
| [List Lists](actions/list-lists.md) | `GET /lists` | [docs](https://developers.sarbacane.com/contacts/#get-all-lists) |
| [List Teams for List](actions/list-teams-for-list.md) | `GET /lists/{listId}/teams` | [docs](https://developers.sarbacane.com/contacts/#list-groups-related-to-a-list) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developers.sarbacane.com/contacts/#get-webhooks) |
| [Manage Campaign Teams](actions/manage-campaign-teams.md) | `PUT /campaigns/{campaignId}/teams` | [docs](https://developers.sarbacane.com/campaigns/#manage-campaigns-teams) |
| [Send Campaign](actions/send-campaign.md) | `POST /campaigns/{campaignId}/send` | [docs](https://developers.sarbacane.com/campaigns/#send-campaign) |
| [Update Contact](actions/update-contact.md) | `PUT /lists/{listId}/contacts/{contactId}` | [docs](https://developers.sarbacane.com/contacts/#edit-a-contact) |
| [Update List](actions/update-list.md) | `PUT /lists/{listId}` | [docs](https://developers.sarbacane.com/contacts/#edit-a-list) |
| [Update Teams for List](actions/update-teams-for-list.md) | `PUT /lists/{listId}/teams` | [docs](https://developers.sarbacane.com/contacts/#edit-groups-related-to-a-list) |
| [Upsert Contact](actions/upsert-contact.md) | `POST /lists/{listId}/contacts/upsert` | [docs](https://developers.sarbacane.com/contacts/#add-edit-a-contact) |
