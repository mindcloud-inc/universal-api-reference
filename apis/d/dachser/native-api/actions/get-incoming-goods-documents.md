# Get Incoming Goods Documents with Dachser

Retrieves incoming goods documents from Dachser.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2/incominggoodsdocuments`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Get Incoming Goods Documents](https://api-portal.dachser.com/bi.b2b.portal/api/library/incominggoodsdocuments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `incoming-goods-number` | query | `string` | no | Incoming goods number. |
| `order-number` | query | `string` | no | Order number. |
| `supplier-number` | query | `string` | no | Supplier number. |
| `supplier-reference-number1` | query | `string` | no | First supplier reference number. |
| `supplier-reference-number2` | query | `string` | no | Second supplier reference number. |
| `branch-number` | query | `number` | no | DACHSER branch number. |
| `date` | query | `date` | no | Incoming goods date. |
