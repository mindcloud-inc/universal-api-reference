# Send Batch Letters with Handwrite

Sends batch letters through Handwrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://api.handwrite.io/v1`
- **Official documentation:** [Send Batch Letters](https://documentation.handwrite.io/#batch-mode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orders[]` | body | `array<object>` | yes | Array of order objects in the same format as Send Letter. Each object can include message, handwriting, card, recipients, and optional from. |
