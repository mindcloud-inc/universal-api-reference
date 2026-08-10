# List Order Payment Transactions with Shopify

## Endpoint

- **Method:** `POST`
- **Path:** `2026-07/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** REST
- **Official documentation:** [List Order Payment Transactions](https://shopify.dev/docs/api/admin-graphql/latest/queries/order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | Order selection inputs. |
| `variables.orderId` | body | `string` | yes | The Shopify GraphQL Order ID to retrieve payment transactions for. |
