# Ontraport: Native API Reference

A consolidated summary of Ontraport's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.ontraport.com/doc/
- **API base URL:** `https://api.ontraport.com/1`

## Authentication

### API Key

Use Ontraport API Key and App ID header credentials.

### Credentials

- **API Key:** `apiKey` · required
- **App ID:** `appId` · required · Your unique Ontraport site ID used with the API key.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://ontraport.com/support/Integrations/obtain-ontraport-api-key-and-app-id)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Pagination

Use `range` in the query string to set the page size (default 50; accepted range 1–50). Use `start` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | `GET /Contacts` | [docs](https://api.ontraport.com/doc/#retrieve-multiple-contacts) |
| [List Messages](actions/list-messages.md) | `GET /Messages` | [docs](https://api.ontraport.com/doc/#retrieve-multiple-messages) |
| [List Products](actions/list-products.md) | `GET /Products` | [docs](https://api.ontraport.com/doc/#retrieve-multiple-products) |
| [List Tags](actions/list-tags.md) | `GET /Tags` | [docs](https://api.ontraport.com/doc/#retrieve-multiple-tags) |
| [List Tasks](actions/list-tasks.md) | `GET /Tasks` | [docs](https://api.ontraport.com/doc/#retrieve-multiple-tasks) |
| [List Transactions](actions/list-transactions.md) | `GET /Transactions` | [docs](https://api.ontraport.com/doc/#retrieve-multiple-transactions) |
| [Retrieve Contact Collection Info](actions/retrieve-contact-collection-info.md) | `GET /Contacts/getInfo` | [docs](https://api.ontraport.com/doc/#retrieve-contact-collection-info) |
| [Retrieve Contact Object Meta](actions/retrieve-contact-object-meta.md) | `GET /Contacts/meta` | [docs](https://api.ontraport.com/doc/#retrieve-contact-object-meta) |
| [Retrieve Message Collection Info](actions/retrieve-message-collection-info.md) | `GET /Messages/getInfo` | [docs](https://api.ontraport.com/doc/#retrieve-message-collection-info) |
| [Retrieve Message Meta](actions/retrieve-message-meta.md) | `GET /Messages/meta` | [docs](https://api.ontraport.com/doc/#retrieve-message-meta) |
| [Retrieve Product Collection Info](actions/retrieve-product-collection-info.md) | `GET /Products/getInfo` | [docs](https://api.ontraport.com/doc/#retrieve-product-collection-info) |
| [Retrieve Product Object Meta](actions/retrieve-product-object-meta.md) | `GET /Products/meta` | [docs](https://api.ontraport.com/doc/#retrieve-product-object-meta) |
| [Retrieve Single Transaction](actions/retrieve-single-transaction.md) | `GET /Transaction` | [docs](https://api.ontraport.com/doc/#retrieve-a-single-transaction) |
| [Retrieve Specific Contact](actions/retrieve-specific-contact.md) | `GET /Contact` | [docs](https://api.ontraport.com/doc/#retrieve-a-specific-contact) |
| [Retrieve Specific Message](actions/retrieve-specific-message.md) | `GET /Message` | [docs](https://api.ontraport.com/doc/#retrieve-a-specific-message) |
| [Retrieve Specific Product](actions/retrieve-specific-product.md) | `GET /Product` | [docs](https://api.ontraport.com/doc/#retrieve-a-specific-product) |
| [Retrieve Specific Tag](actions/retrieve-specific-tag.md) | `GET /Tag` | [docs](https://api.ontraport.com/doc/#retrieve-a-specific-tag) |
| [Retrieve Specific Task](actions/retrieve-specific-task.md) | `GET /Task` | [docs](https://api.ontraport.com/doc/#retrieve-a-specific-task) |
| [Retrieve Tag Collection Info](actions/retrieve-tag-collection-info.md) | `GET /Tags/getInfo` | [docs](https://api.ontraport.com/doc/#retrieve-tag-collection-info) |
| [Retrieve Tag Object Meta](actions/retrieve-tag-object-meta.md) | `GET /Tags/meta` | [docs](https://api.ontraport.com/doc/#retrieve-tag-object-meta) |
| [Retrieve Task Collection Info](actions/retrieve-task-collection-info.md) | `GET /Tasks/getInfo` | [docs](https://api.ontraport.com/doc/#retrieve-task-collection-info) |
| [Retrieve Task Object Meta](actions/retrieve-task-object-meta.md) | `GET /Tasks/meta` | [docs](https://api.ontraport.com/doc/#retrieve-task-object-meta) |
| [Retrieve Transaction Collection Info](actions/retrieve-transaction-collection-info.md) | `GET /Invoices/getInfo` | [docs](https://api.ontraport.com/doc/#retrieve-transaction-collection-info) |
| [Retrieve Transaction Object Meta](actions/retrieve-transaction-object-meta.md) | `GET /Transactions/meta` | [docs](https://api.ontraport.com/doc/#retrieve-transaction-object-meta) |
