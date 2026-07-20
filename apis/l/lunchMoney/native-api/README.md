# Lunch Money: Native API Reference

A consolidated summary of Lunch Money's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://alpha.lunchmoney.dev/v2/docs
- **OpenAPI specification:** https://alpha.lunchmoney.dev/v2/openapi
- **API base URL:** `https://api.lunchmoney.dev/v2`

## Authentication

### API Key

Use a Lunch Money personal access token. MindCloud uses the implicit apiKey credential contract and sends it as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://alpha.lunchmoney.dev/v2/getting-started)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 1000; accepted range 1–2000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Attach a file to a transaction](actions/attach-file-to-transaction.md) | `POST /transactions/:transaction_id/attachments` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Create a new category or category group](actions/create-category.md) | `POST /categories` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Create a manual account](actions/create-manual-account.md) | `POST /manual_accounts` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Create transactions](actions/create-new-transactions.md) | `POST /transactions` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Create a new tag](actions/create-tag.md) | `POST /tags` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Delete budget](actions/delete-budget.md) | `DELETE /budgets` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Delete a category or category group](actions/delete-category.md) | `DELETE /categories/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Delete a manual account](actions/delete-manual-account.md) | `DELETE /manual_accounts/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Delete a tag](actions/delete-tag.md) | `DELETE /tags/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Delete a file attachment](actions/delete-transaction-attachment.md) | `DELETE /transactions/attachments/:file_id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Delete a transaction](actions/delete-transaction-by-id.md) | `DELETE /transactions/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Bulk delete existing transactions](actions/delete-transactions.md) | `DELETE /transactions` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Get all categories](actions/get-all-categories.md) | `GET /categories` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Get all manual accounts](actions/get-all-manual-accounts.md) | `GET /manual_accounts` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Get all accounts synced via Plaid](actions/get-all-plaid-accounts.md) | `GET /plaid_accounts` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Get all recurring items](actions/get-all-recurring.md) | `GET /recurring_items` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Get all tags](actions/get-all-tags.md) | `GET /tags` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Get all transactions](actions/get-all-transactions.md) | `GET /transactions` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Get budget settings](actions/get-budget-settings.md) | `GET /budgets/settings` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Get budget summary](actions/get-budget-summary.md) | `GET /summary` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Get a single category](actions/get-category-by-id.md) | `GET /categories/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Get a single manual account](actions/get-manual-account-by-id.md) | `GET /manual_accounts/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Get current user](actions/get-me.md) | `GET /me` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Get a single tag](actions/get-tag-by-id.md) | `GET /tags/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Get transaction attachment download URL](actions/get-transaction-attachment-url.md) | `GET /transactions/attachments/:file_id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Get a single transaction](actions/get-transaction-by-id.md) | `GET /transactions/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Create a transaction group](actions/group-transactions.md) | `POST /transactions/group` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Split a transaction](actions/split-transaction.md) | `POST /transactions/split/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Delete a transaction group](actions/ungroup-transactions.md) | `DELETE /transactions/group/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Unsplit a transaction](actions/unsplit-transaction.md) | `DELETE /transactions/split/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Update an existing category or category group](actions/update-category.md) | `PUT /categories/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Update an existing manual account](actions/update-manual-account.md) | `PUT /manual_accounts/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Update an existing tag](actions/update-tag.md) | `PUT /tags/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Update an existing transaction](actions/update-transaction.md) | `PUT /transactions/:id` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Update multiple transactions](actions/update-transactions.md) | `PUT /transactions` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
| [Upsert budget](actions/upsert-budget.md) | `PUT /budgets` | [docs](https://alpha.lunchmoney.dev/v2/docs) |
