# Import Customer Payment Conditions with Order Sender

Imports customer payment conditions into Order Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/op/import/res/clienti_pagamenti`
- **Base URL:** `https://business.ordersender.com/api/v1`
- **Official documentation:** [Import Customer Payment Conditions](https://developer.ordersender.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `records` | body | `string` | no | Array of customer payment condition records to import. |
