# List Payment Conditions with Order Sender

Retrieves payment conditions from Order Sender.

## Endpoint

- **Method:** `GET`
- **Path:** `/op/export/res/condizioni_pagamento`
- **Base URL:** `https://business.ordersender.com/api/v1`
- **Official documentation:** [List Payment Conditions](https://developer.ordersender.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `delimiter` | query | `string` | no | Delimiter used only when requesting CSV output. |
| `format` | query | `string` | no | Response format. Use json for structured records. |
| `fornitore` | query | `string` | no | Optional supplier code filter. |
