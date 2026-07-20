# Import Commissions with Order Sender

Imports commission records into Order Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/op/import/res/provvigioni`
- **Base URL:** `https://business.ordersender.com/api/v1`
- **Official documentation:** [Import Commissions](https://developer.ordersender.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `records` | body | `string` | no | Array of commission records to import. |
