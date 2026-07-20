# Import Payment Conditions with Order Sender

Imports payment conditions into Order Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/op/import/res/condizioni_pagamento`
- **Base URL:** `https://business.ordersender.com/api/v1`
- **Official documentation:** [Import Payment Conditions](https://developer.ordersender.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `records` | body | `string` | no | Array of payment condition records to import. |
