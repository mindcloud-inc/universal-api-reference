# List Products with MailBluster

Retrieves a page of products from MailBluster.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://api.mailbluster.com/api`
- **Official documentation:** [List Products](https://app.mailbluster.com/api-doc/products/read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageNo` | query | `number` | no | Page number to retrieve. |
| `perPage` | query | `number` | no | Number of products to retrieve per page. |
