# Farmbrite: Native API Reference

A consolidated summary of Farmbrite's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://developers.farmbrite.com/docs/
- **OpenAPI specification:** https://developers.farmbrite.com/docs/openapi.json
- **API base URL:** `https://api.farmbrite.com/v1`

## Authentication

### API Key

Use a Farmbrite personal access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.farmbrite.com/docs/)

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_dir`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create animal](actions/create-animal.md) | `POST /animals` | [docs](https://developers.farmbrite.com/docs/) |
| [Create contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.farmbrite.com/docs/) |
| [Create order](actions/create-order.md) | `POST /orders` | [docs](https://developers.farmbrite.com/docs/) |
| [Create plot](actions/create-plot.md) | `POST /plots` | [docs](https://developers.farmbrite.com/docs/) |
| [Create product](actions/create-product.md) | `POST /products` | [docs](https://developers.farmbrite.com/docs/) |
| [Create task](actions/create-task.md) | `POST /tasks` | [docs](https://developers.farmbrite.com/docs/) |
| [Create tool](actions/create-tool.md) | `POST /tools` | [docs](https://developers.farmbrite.com/docs/) |
| [Create transaction](actions/create-transaction.md) | `POST /transactions` | [docs](https://developers.farmbrite.com/docs/) |
| [Delete animal](actions/delete-animal.md) | `DELETE /animals/:animal_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Delete contact](actions/delete-contact.md) | `DELETE /contacts/:contact_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Delete order](actions/delete-order.md) | `DELETE /orders/:order_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Delete plot](actions/delete-plot.md) | `DELETE /plots/:plot_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Delete product](actions/delete-product.md) | `DELETE /products/:product_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Delete task](actions/delete-task.md) | `DELETE /tasks/:task_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Delete tool](actions/delete-tool.md) | `DELETE /tools/:tool_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Delete transaction](actions/delete-transaction.md) | `DELETE /transactions/:transaction_id` | [docs](https://developers.farmbrite.com/docs/) |
| [List animals](actions/list-animals.md) | `GET /animals` | [docs](https://developers.farmbrite.com/docs/) |
| [List contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.farmbrite.com/docs/) |
| [List orders](actions/list-orders.md) | `GET /orders` | [docs](https://developers.farmbrite.com/docs/) |
| [List plots](actions/list-plots.md) | `GET /plots` | [docs](https://developers.farmbrite.com/docs/) |
| [List products](actions/list-products.md) | `GET /products` | [docs](https://developers.farmbrite.com/docs/) |
| [List tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://developers.farmbrite.com/docs/) |
| [List tools](actions/list-tools.md) | `GET /tools` | [docs](https://developers.farmbrite.com/docs/) |
| [List transactions](actions/list-transactions.md) | `GET /transactions` | [docs](https://developers.farmbrite.com/docs/) |
| [Retrieve animal](actions/retrieve-animal.md) | `GET /animals/:animal_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Retrieve contact](actions/retrieve-contact.md) | `GET /contacts/:contact_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Retrieve order](actions/retrieve-order.md) | `GET /orders/:order_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Retrieve plot](actions/retrieve-plot.md) | `GET /plots/:plot_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Retrieve product](actions/retrieve-product.md) | `GET /products/:product_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Retrieve task](actions/retrieve-task.md) | `GET /tasks/:task_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Retrieve tool](actions/retrieve-tool.md) | `GET /tools/:tool_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Retrieve transaction](actions/retrieve-transaction.md) | `GET /transactions/:transaction_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Update animal](actions/update-animal.md) | `PUT /animals/:animal_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Update contact](actions/update-contact.md) | `PUT /contacts/:contact_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Update plot](actions/update-plot.md) | `PUT /plots/:plot_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Update product](actions/update-product.md) | `PUT /products/:product_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Update task](actions/update-task.md) | `PUT /tasks/:task_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Update tool](actions/update-tool.md) | `PUT /tools/:tool_id` | [docs](https://developers.farmbrite.com/docs/) |
| [Update transaction](actions/update-transaction.md) | `PUT /transactions/:transaction_id` | [docs](https://developers.farmbrite.com/docs/) |
