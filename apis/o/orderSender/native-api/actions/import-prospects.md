# Import Prospects with Order Sender

Imports prospect records into Order Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/op/import/res/prospect`
- **Base URL:** `https://business.ordersender.com/api/v1`
- **Official documentation:** [Import Prospects](https://developer.ordersender.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `records` | body | `string` | no | Array of prospect records to import. |
