# List Price Lists with Order Sender

Retrieves price lists from Order Sender.

## Endpoint

- **Method:** `GET`
- **Path:** `/op/export/res/listini`
- **Base URL:** `https://business.ordersender.com/api/v1`
- **Official documentation:** [List Price Lists](https://developer.ordersender.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `delimiter` | query | `string` | no | Delimiter used only when requesting CSV output. |
| `format` | query | `string` | no | Response format. Use json for structured records. |
| `fornitore` | query | `string` | no | Optional supplier code filter. |
