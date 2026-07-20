# List Products with Whop

Retrieves products from Whop for a company.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/products`
- **Base URL:** `https://api.whop.com`
- **Official documentation:** [List Products](https://docs.whop.com/api-reference/products/list-products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | query | `string` | yes | The unique identifier of the company to list products for. |
