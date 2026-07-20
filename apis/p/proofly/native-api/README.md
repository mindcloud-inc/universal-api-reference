# Proofly: Native API Reference

A consolidated summary of Proofly's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://proofly.io/developers
- **API base URL:** `https://proofly.io/api`

## Authentication

### API Key

Authenticate with your Proofly API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://proofly.io/developers)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | `GET /campaign/:campaignId` | [docs](https://proofly.io/developers#api-method-campaign) |
| [Get Notification Data](actions/get-notification-data.md) | `GET /data/:notificationId` | [docs](https://proofly.io/developers#api-method-data) |
| [Get User](actions/get-user.md) | `GET /user` | [docs](https://proofly.io/developers#api-method-user) |
| [List Activity](actions/list-activity.md) | `GET /activity` | [docs](https://proofly.io/developers#api-method-activity) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://proofly.io/developers#api-method-campaigns) |
| [Toggle Campaign](actions/toggle-campaign.md) | `PUT /campaign/:campaignId` | [docs](https://proofly.io/developers#api-method-campaign-toggle) |
