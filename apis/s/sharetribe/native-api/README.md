# Sharetribe: Native API Reference

A consolidated summary of Sharetribe's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://www.sharetribe.com/api-reference/integration.html
- **API base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`

## Authentication

### OAuth2 (Client Credentials)

Machine-to-machine OAuth2 client credentials flow for the Sharetribe Integration API.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://flex-api.sharetribe.com/v1/auth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `integ`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://flex-api.sharetribe.com/v1/auth/token. A machine-to-machine flow is configured.

[Official authentication documentation](https://www.sharetribe.com/api-reference/authentication.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `meta.totalPages`. The current page number is read from `meta.page`.

## Pagination

Use `perPage` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Approve Listing](actions/approve-listing.md) | `POST listings/approve` | [docs](https://www.sharetribe.com/api-reference/integration.html#approve-listing) |
| [Approve User](actions/approve-user.md) | `POST users/approve` | [docs](https://www.sharetribe.com/api-reference/integration.html#approve-user) |
| [Close Listing](actions/close-listing.md) | `POST listings/close` | [docs](https://www.sharetribe.com/api-reference/integration.html#close-listing) |
| [Create Availability Exceptions](actions/create-availability-exceptions.md) | `POST availability_exceptions/create` | [docs](https://www.sharetribe.com/api-reference/integration.html#create-availability-exceptions) |
| [Create Listing](actions/create-listing.md) | `POST listings/create` | [docs](https://www.sharetribe.com/api-reference/integration.html#create-listing) |
| [Create Stock Adjustment](actions/create-stock-adjustment.md) | `POST stock_adjustments/create` | [docs](https://www.sharetribe.com/api-reference/integration.html#create-stock-adjustment) |
| [Delete Availability Exceptions](actions/delete-availability-exceptions.md) | `POST availability_exceptions/delete` | [docs](https://www.sharetribe.com/api-reference/integration.html#delete-availability-exceptions) |
| [Open Listing](actions/open-listing.md) | `POST listings/open` | [docs](https://www.sharetribe.com/api-reference/integration.html#open-listing) |
| [Query Availability Exceptions](actions/query-availability-exceptions.md) | `GET availability_exceptions/query` | [docs](https://www.sharetribe.com/api-reference/integration.html#query-availability-exceptions) |
| [Query Events](actions/query-events.md) | `GET events/query` | [docs](https://www.sharetribe.com/api-reference/integration.html#query-events) |
| [Query Listings](actions/query-listings.md) | `GET listings/query` | [docs](https://www.sharetribe.com/api-reference/integration.html#query-listings) |
| [Query Stock Adjustments](actions/query-stock-adjustments.md) | `GET stock_adjustments/query` | [docs](https://www.sharetribe.com/api-reference/integration.html#query-stock-adjustments) |
| [Query Transactions](actions/query-transactions.md) | `GET transactions/query` | [docs](https://www.sharetribe.com/api-reference/integration.html#query-transactions) |
| [Query Users](actions/query-users.md) | `GET users/query` | [docs](https://www.sharetribe.com/api-reference/integration.html#query-users) |
| [Show Listing](actions/show-listing.md) | `GET listings/show` | [docs](https://www.sharetribe.com/api-reference/integration.html#show-listing) |
| [Show Transaction](actions/show-transaction.md) | `GET transactions/show` | [docs](https://www.sharetribe.com/api-reference/integration.html#show-transaction) |
| [Show User](actions/show-user.md) | `GET users/show` | [docs](https://www.sharetribe.com/api-reference/integration.html#show-user) |
| [Speculatively Transition Transaction](actions/speculatively-transition-transaction.md) | `POST transactions/transition_speculative` | [docs](https://www.sharetribe.com/api-reference/integration.html#speculatively-transition-transaction) |
| [Transition Transaction](actions/transition-transaction.md) | `POST transactions/transition` | [docs](https://www.sharetribe.com/api-reference/integration.html#transition-transaction) |
| [Update Listing](actions/update-listing.md) | `POST listings/update` | [docs](https://www.sharetribe.com/api-reference/integration.html#update-listing) |
| [Update Transaction Metadata](actions/update-transaction-metadata.md) | `POST transactions/update_metadata` | [docs](https://www.sharetribe.com/api-reference/integration.html#update-transaction-metadata) |
| [Update User Profile](actions/update-user-profile.md) | `POST users/update_profile` | [docs](https://www.sharetribe.com/api-reference/integration.html#update-user-profile) |
| [Upload Image](actions/upload-image.md) | `POST images/upload` | [docs](https://www.sharetribe.com/api-reference/integration.html#upload-image) |
