# Import Suppliers with Order Sender

Imports supplier records into Order Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/op/import/res/fornitori`
- **Base URL:** `https://business.ordersender.com/api/v1`
- **Official documentation:** [Import Suppliers](https://developer.ordersender.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `records` | body | `string` | no | Array of supplier records to import. |
