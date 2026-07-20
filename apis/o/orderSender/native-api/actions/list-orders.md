# List Orders with Order Sender

Retrieves sales orders from Order Sender.

## Endpoint

- **Method:** `GET`
- **Path:** `/op/export/res/ordini`
- **Base URL:** `https://business.ordersender.com/api/v1`
- **Official documentation:** [List Orders](https://developer.ordersender.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | query | `string` | no | Export start date in YYYY-MM-DD format. |
| `dateTo` | query | `string` | no | Export end date in YYYY-MM-DD format. |
| `delimiter` | query | `string` | no | Delimiter used only when requesting CSV output. |
| `format` | query | `string` | no | Response format. Use json for structured records. |
| `fornitore` | query | `string` | no | Optional supplier code filter. |
| `ids` | query | `string` | no | Optional comma-separated order numbers filter. |
| `NumOrdFrom` | query | `string` | no | Optional start order number filter. |
| `NumOrdTo` | query | `string` | no | Optional end order number filter. |
