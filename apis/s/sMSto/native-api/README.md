# SMS.to: Native API Reference

A consolidated summary of SMS.to's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.sms.to/
- **API base URL:** `https://api.sms.to`

## Authentication

### API Key

Use an SMS.to API key with Bearer auth

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.sms.to/support/solutions/articles/43000515639-sms-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Estimate Campaign Message](actions/estimate-campaign-message.md) | `POST /sms/estimate` | [docs](https://developers.sms.to/#ee7a8f3c-d4bb-4cd0-a6ce-3b62c3f9530f) |
| [Estimate Campaign Viber](actions/estimate-campaign-viber.md) | `POST /viber/estimate` | [docs](https://developers.sms.to/#cf0b6175-236b-4a47-bc8b-1bab933373df) |
| [Estimate List Message](actions/estimate-list-message.md) | `POST /sms/estimate` | [docs](https://developers.sms.to/#34aedb6e-3d81-409e-a485-75c41f32fa04) |
| [Estimate Personalized Message](actions/estimate-personalized-message.md) | `POST /sms/estimate` | [docs](https://developers.sms.to/#2c63629b-5414-48ef-8b9b-cd902c23275d) |
| [Estimate Single Message](actions/estimate-single-message.md) | `POST /sms/estimate` | [docs](https://developers.sms.to/#dee1f2ba-a154-43da-aa88-80cd4841a6da) |
| [Estimate Single Message Legacy GET](actions/estimate-single-message-legacy-get.md) | `GET /sms/estimate` | [docs](https://developers.sms.to/#1e976374-8553-45e3-b84b-388494d7cb7b) |
| [Estimate Single Viber Message](actions/estimate-single-viber-message.md) | `POST /viber/estimate` | [docs](https://developers.sms.to/#13d6ed83-cc16-4d78-a26f-50ce942eb58d) |
| [Get Campaign by ID](actions/get-campaign-by-id.md) | `GET /v2/campaigns/:id` | [docs](https://developers.sms.to/#6325eaae-8d7c-434d-aca4-0ba43e04dbc6) |
| [Get Last Campaign](actions/get-last-campaign.md) | `GET /v2/last/campaign` | [docs](https://developers.sms.to/#d66885d4-85eb-4474-9e86-943ed90ee3fb) |
| [Get Last Message](actions/get-last-message.md) | `GET /v2/last/message` | [docs](https://developers.sms.to/#f168467f-e0fe-463f-a949-34801631fcc5) |
| [Get Message by ID](actions/get-message-by-id.md) | `GET /message/:id` | [docs](https://developers.sms.to/#eb39c6ad-e1c8-4a6a-8d2d-f04122315fb3) |
| [List Campaigns](actions/list-campaigns.md) | `GET /v2/campaigns` | [docs](https://developers.sms.to/#2f2808c0-9b89-4cc9-8364-e1cae3f8a83f) |
| [List Messages](actions/list-messages.md) | `GET /v2/messages` | [docs](https://developers.sms.to/#4bcab664-aa65-4abc-b5f4-7f3037dbadcb) |
| [Monthly Usage Report](actions/monthly-usage-report.md) | `POST /v1/reports/monthly-usage` | [docs](https://developers.sms.to/#f1fe0830-0200-45ec-b81f-f09e3977a479) |
| [Schedule Sending Messages](actions/schedule-sending-messages.md) | `POST /sms/send` | [docs](https://developers.sms.to/#32162af7-26e0-485a-87a4-d94ab6cdd1ba) |
| [Schedule Sending Viber Messages](actions/schedule-sending-viber-messages.md) | `POST /viber/send` | [docs](https://developers.sms.to/#c8047d14-7907-4207-b61d-57b284609df2) |
| [Send Campaign Message](actions/send-campaign-message.md) | `POST /sms/send` | [docs](https://developers.sms.to/#436bf9d3-0c63-48ac-9a54-91f7d239a86f) |
| [Send Campaign Viber](actions/send-campaign-viber.md) | `POST /viber/send` | [docs](https://developers.sms.to/#84e486e1-a3d6-4eab-be1b-111d3ada129f) |
| [Send Flash Message](actions/send-flash-message.md) | `POST /fsms/send` | [docs](https://developers.sms.to/#f166ed5d-c461-471c-be14-8d79d61049b8) |
| [Send Message to a List or Multiple List in Array](actions/send-message-to-a-list-or-multiple-list-in-array.md) | `POST /sms/send` | [docs](https://developers.sms.to/#5ccea815-9f65-428f-8c17-97514825b4b4) |
| [Send Personalized Messages](actions/send-personalized-messages.md) | `POST /sms/send` | [docs](https://developers.sms.to/#7abcccad-8066-403e-9bfc-515e3bd6f8f2) |
| [Send Single Message](actions/send-single-message.md) | `POST /sms/send` | [docs](https://developers.sms.to/#3a12f9ae-8afa-4d15-a3c5-4895c3a14778) |
| [Send Viber Message](actions/send-viber-message.md) | `POST /viber/send` | [docs](https://developers.sms.to/#fd60cb4c-3baa-4d9f-9e59-e93695357133) |
| [Send Viber to a List/s](actions/send-viber-to-a-lists.md) | `POST /viber/send` | [docs](https://developers.sms.to/#1c01abb9-f7dc-4dfc-9481-6bb5e31f4c97) |
