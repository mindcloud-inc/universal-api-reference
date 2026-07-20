# List Suppliers with Order Sender

Retrieves supplier records from Order Sender.

## Endpoint

- **Method:** `GET`
- **Path:** `/op/export/res/fornitori`
- **Base URL:** `https://business.ordersender.com/api/v1`
- **Official documentation:** [List Suppliers](https://developer.ordersender.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `delimiter` | query | `string` | no | Delimiter used only when requesting CSV output. |
| `format` | query | `string` | no | Response format. Use json for structured records. |
