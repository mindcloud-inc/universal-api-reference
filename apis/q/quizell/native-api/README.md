# Quizell: Native API Reference

A consolidated summary of Quizell's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://docs.quizell.com
- **API base URL:** `https://api.quizell.com/api/v1`

## Authentication

### API Key

Connect Quizell with an API key from Integrations -> APIs.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.quizell.com/en/article/how-to-find-and-generate-your-api-key-in-quizell-1gpeq3w/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `per_page` in the query string to set the page size (default 10; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Products](actions/batch-products.md) | `POST /products/batch` | [docs](https://docs.quizell.com/product-apis#post-multiple-product) |
| [Create Customer](actions/create-customer.md) | `POST /customers/store` | [docs](https://docs.quizell.com/customer-apis#create-customer) |
| [Create Customer Custom Field](actions/create-customer-custom-field.md) | `POST /customers/custom_fields/store` | [docs](https://docs.quizell.com/customer-apis#create-customers-custom-fields) |
| [Create Product](actions/create-product.md) | `POST /products/store` | [docs](https://docs.quizell.com/product-apis#create-product) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/delete/:lead_id` | [docs](https://docs.quizell.com/customer-apis#delete-customer) |
| [Delete Customer Custom Field](actions/delete-customer-custom-field.md) | `DELETE /customers/custom_fields/delete/:field_id` | [docs](https://docs.quizell.com/customer-apis#delete-customers-custom-fields) |
| [Delete Multiple Products](actions/delete-multiple-products.md) | `DELETE /products/delete/multiple` | [docs](https://docs.quizell.com/product-apis#delete-multiple-product) |
| [Delete Product](actions/delete-product.md) | `DELETE /products/delete/single/:product_id` | [docs](https://docs.quizell.com/product-apis#delete-product) |
| [Get Customer](actions/get-customer.md) | `GET /customers/detail/:lead_id` | [docs](https://docs.quizell.com/customer-apis#get-customer-details) |
| [Get Product](actions/get-product.md) | `GET /products/:product_id/show` | [docs](https://docs.quizell.com/product-apis#get-product) |
| [List Customer Custom Fields](actions/list-customer-custom-fields.md) | `GET /customers/custom_fields/list` | [docs](https://docs.quizell.com/customer-apis#customers-custom-fields-list) |
| [List Customers](actions/list-customers.md) | `GET /customers/list` | [docs](https://docs.quizell.com/customer-apis#list-customers) |
| [Search Products](actions/search-products.md) | `GET /products/search` | [docs](https://docs.quizell.com/product-apis#search-product) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/update/:lead_id` | [docs](https://docs.quizell.com/customer-apis#update-customer) |
| [Update Product](actions/update-product.md) | `PUT /products/update/:product_id` | [docs](https://docs.quizell.com/product-apis#update-product) |
