# Fidel API: Native API Reference

A consolidated summary of Fidel API's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.fidelapi.com/docs/select
- **API base URL:** `https://api.fidel.uk/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Fidel-Key: <apiKey>
```

[Official authentication documentation](https://docs.fidelapi.com/docs/select/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `start` in the query string as the pagination cursor.

## Sorting

Set the sort field with `order` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Offer on Card](actions/activate-offer-on-card.md) | `POST /offers/:offerId/cards/:cardId` | [docs](https://reference.fidel.uk/reference/activate-offer-on-card) |
| [Create Brand](actions/create-brand.md) | `POST /brands` | [docs](https://reference.fidel.uk/reference/create-brand) |
| [Create Card](actions/create-card.md) | `POST /programs/:programId/cards` | [docs](https://reference.fidel.uk/reference/create-card) |
| [Create Location](actions/create-location.md) | `POST /programs/:programId/locations` | [docs](https://reference.fidel.uk/reference/create-location) |
| [Create MID Request](actions/create-mid-request.md) | `POST /programs/:programId/mid-requests` | [docs](https://docs.fidelapi.com/docs/select/mid-management#mid-requests) |
| [Create Missing Transaction Request](actions/create-missing-transaction-request.md) | `POST /cards/:cardId/missing-transaction-requests` | [docs](https://reference.fidel.uk/reference/create-missing-transaction-request) |
| [Create Offer](actions/create-offer.md) | `POST /offers` | [docs](https://reference.fidel.uk/reference/create-offer) |
| [Create Program](actions/create-program.md) | `POST /programs` | [docs](https://reference.fidel.uk/reference/create-program) |
| [Create Webhook (Program)](actions/create-webhook-program.md) | `POST /programs/:programId/hooks` | [docs](https://reference.fidel.uk/reference/create-webhook-program) |
| [Delete Offer](actions/delete-offer.md) | `DELETE /offers/:offerId` | [docs](https://reference.fidel.uk/reference/delete-offer) |
| [Get Brand](actions/get-brand.md) | `GET /brands/:brandId` | [docs](https://reference.fidel.uk/reference/get-brand) |
| [Get Card](actions/get-card.md) | `GET /cards/:cardId` | [docs](https://reference.fidel.uk/reference/get-card) |
| [Get Location](actions/get-location.md) | `GET /locations/:locationId` | [docs](https://reference.fidel.uk/reference/get-location) |
| [Get MID](actions/get-mid.md) | `GET /programs/:programId/mids/:midId` | [docs](https://reference.fidel.uk/reference/get-mid) |
| [Get MID Request](actions/get-mid-request.md) | `GET /programs/:programId/mid-requests/:midRequestId` | [docs](https://reference.fidel.uk/reference/get-mid-request) |
| [Get Missing Transaction Request](actions/get-missing-transaction-request.md) | `GET /missing-transaction-requests/:missingTransactionRequestId` | [docs](https://reference.fidel.uk/reference/get_missing-transaction-requests-missingtransactionrequestid) |
| [Get Offer](actions/get-offer.md) | `GET /offers/:offerId` | [docs](https://reference.fidel.uk/reference/get-offer) |
| [Get Program](actions/get-program.md) | `GET /programs/:programId` | [docs](https://reference.fidel.uk/reference/get-program) |
| [Get Transaction](actions/get-transaction.md) | `GET /transactions/:transactionId` | [docs](https://reference.fidel.uk/reference/get-transaction) |
| [Get Webhook](actions/get-webhook.md) | `GET /hooks/:hookId` | [docs](https://reference.fidel.uk/reference/get-webhook) |
| [Link Location to Offer](actions/link-location-to-offer.md) | `POST /offers/:offerId/locations/:locationId` | [docs](https://reference.fidel.uk/reference/link-location-to-offer) |
| [List Brands](actions/list-brands.md) | `GET /brands` | [docs](https://reference.fidel.uk/reference/list-brands) |
| [List Cards](actions/list-cards.md) | `GET /programs/:programId/cards` | [docs](https://reference.fidel.uk/reference/list-cards) |
| [List Locations](actions/list-locations.md) | `GET /programs/:programId/locations` | [docs](https://reference.fidel.uk/reference/list-locations) |
| [List Locations by Brand](actions/list-locations-by-brand.md) | `GET /brands/:brandId/programs/:programId/locations` | [docs](https://reference.fidel.uk/reference/list-locations-by-brand) |
| [List MID Requests](actions/list-mid-requests.md) | `GET /programs/:programId/mid-requests` | [docs](https://reference.fidel.uk/reference/list-mid-requests) |
| [List MIDs](actions/list-mids.md) | `GET /programs/:programId/mids` | [docs](https://reference.fidel.uk/reference/list-mids) |
| [List Missing Transaction Requests](actions/list-missing-transaction-requests.md) | `GET /programs/:programId/missing-transaction-requests` | [docs](https://reference.fidel.uk/reference/list-missing-transaction-request) |
| [List Offers](actions/list-offers.md) | `GET /offers` | [docs](https://reference.fidel.uk/reference/list-offers) |
| [List Programs](actions/list-programs.md) | `GET /programs` | [docs](https://reference.fidel.uk/reference/list-programs) |
| [List Transactions by Card](actions/list-transactions-by-card.md) | `GET /cards/:cardId/transactions` | [docs](https://reference.fidel.uk/reference/list-transactions-by-card) |
| [List Transactions by Program](actions/list-transactions-by-program.md) | `GET /programs/:programId/transactions` | [docs](https://reference.fidel.uk/reference/list-transactions) |
| [List Webhooks](actions/list-webhooks.md) | `GET /programs/:programId/hooks` | [docs](https://reference.fidel.uk/reference/list-webhooks) |
| [Sync Program](actions/sync-program.md) | `PUT /programs/:programId` | [docs](https://reference.fidel.uk/reference/sync-program) |
| [Update Brand](actions/update-brand.md) | `PATCH /brands/:brandId` | [docs](https://reference.fidel.uk/reference/update-brand) |
| [Update Card Metadata](actions/update-card-metadata.md) | `PUT /cards/:cardId/metadata` | [docs](https://reference.fidel.uk/reference/update-card-metadata) |
| [Update Location](actions/update-location.md) | `PATCH /locations/:locationId` | [docs](https://reference.fidel.uk/reference/update-location) |
| [Update Offer](actions/update-offer.md) | `PATCH /offers/:offerId` | [docs](https://reference.fidel.uk/reference/edit-offer) |
| [Update Program](actions/update-program.md) | `PATCH /programs/:programId` | [docs](https://reference.fidel.uk/reference/update-program) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /hooks/:hookId` | [docs](https://reference.fidel.uk/reference/update-webhook) |
