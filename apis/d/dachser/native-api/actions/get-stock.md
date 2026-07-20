# Get Stock with Dachser

Retrieves stock records from Dachser by article or warehouse.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2/stocks`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Get Stock](https://api-portal.dachser.com/bi.b2b.portal/api/library/stock)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `article-number` | query | `string` | no | Filter on article number. |
| `product-variant` | query | `number` | no | Filter on product variant. |
| `lot` | query | `string` | no | Filter on lot number. |
| `variable-classification` | query | `number` | no | Filter on variable classification. |
| `blocking-reason` | query | `number` | no | Filter on blocking reason. |
| `best-before-date` | query | `date` | no | Filter on best-before date. |
| `customer-id` | query | `string` | no | Customer number. |
| `branch-id` | query | `string` | no | Warehouse or branch number. |
| `acceptLanguage` | query | `string` | no | Optional language sent as the Accept-Language header. |
| `accept` | query | `string` | no | Optional Accept header value. |
