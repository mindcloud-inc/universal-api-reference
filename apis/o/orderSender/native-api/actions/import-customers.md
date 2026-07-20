# Import Customers with Order Sender

Imports customer records into Order Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/op/import/res/clienti`
- **Base URL:** `https://business.ordersender.com/api/v1`
- **Official documentation:** [Import Customers](https://developer.ordersender.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `records` | body | `string` | no | Array of customer records to import. |
