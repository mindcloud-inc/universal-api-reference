# HeyPoplar: Native API Reference

A consolidated summary of HeyPoplar's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://docs.heypoplar.com/api
- **API base URL:** `https://api.heypoplar.com/v1`

## Authentication

### Access Token

Authenticate with a Poplar bearer access token generated from the account API page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.heypoplar.com/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 5; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Do Not Mail Entry](actions/add-do-not-mail-entry.md) | `POST /do-not-mail` | [docs](https://docs.heypoplar.com/api/endpoints/do-not-mail) |
| [Create Audience Member](actions/create-audience-member.md) | `POST /audience/:id` | [docs](https://docs.heypoplar.com/api/endpoints/audience#create-audience-member) |
| [Create Data Subject Request](actions/create-data-subject-request.md) | `POST /dsr/request` | [docs](https://docs.heypoplar.com/api/endpoints/data-subject-requests#create-data-subject-request) |
| [Create Mailer](actions/create-mailer.md) | `POST /mailing` | [docs](https://docs.heypoplar.com/api/endpoints/mailing#create-mailer) |
| [Create Order](actions/create-order.md) | `POST /order` | [docs](https://docs.heypoplar.com/api/endpoints/orders#submit-order) |
| [Delete Order](actions/delete-order.md) | `DELETE /order/:order_id` | [docs](https://docs.heypoplar.com/api/endpoints/orders#delete-order) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaign/:id` | [docs](https://docs.heypoplar.com/api/endpoints/other-endpoints#fetch-campaign) |
| [Get Current Organization](actions/get-current-organization.md) | `GET /me` | [docs](https://docs.heypoplar.com/api/endpoints/other-endpoints#fetch-current-organization) |
| [Get Data Subject Request Status](actions/get-data-subject-request-status.md) | `GET /dsr/request/:subject_request_id` | [docs](https://docs.heypoplar.com/api/endpoints/data-subject-requests#fetch-data-subject-request-status) |
| [Get Mailing](actions/get-mailing.md) | `GET /mailing/:mailing_id` | [docs](https://docs.heypoplar.com/api/endpoints/mailing#fetch-mailing) |
| [List Active Campaigns](actions/list-active-campaigns.md) | `GET /campaigns` | [docs](https://docs.heypoplar.com/api/endpoints/other-endpoints#fetch-active-campaigns) |
| [List Audiences](actions/list-audiences.md) | `GET /audiences` | [docs](https://docs.heypoplar.com/api/endpoints/audience#fetch-audiences) |
| [List Campaign Creatives](actions/list-campaign-creatives.md) | `GET /campaign/:id/creatives` | [docs](https://docs.heypoplar.com/api/endpoints/other-endpoints#fetch-campaign-creatives) |
| [List Campaign Mailings](actions/list-campaign-mailings.md) | `GET /campaign/:id/mailings` | [docs](https://docs.heypoplar.com/api/endpoints/other-endpoints#fetch-campaign-mailings) |
| [Update Order](actions/update-order.md) | `POST /order/:order_id` | [docs](https://docs.heypoplar.com/api/endpoints/orders#edit-order) |
