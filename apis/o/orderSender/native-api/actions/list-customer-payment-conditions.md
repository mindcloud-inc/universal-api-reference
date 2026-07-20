# List Customer Payment Conditions with Order Sender

Retrieves customer payment conditions from Order Sender.

## Endpoint

- **Method:** `GET`
- **Path:** `/op/export/res/clienti_pagamenti`
- **Base URL:** `https://business.ordersender.com/api/v1`
- **Official documentation:** [List Customer Payment Conditions](https://developer.ordersender.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `delimiter` | query | `string` | no | Delimiter used only when requesting CSV output. |
| `format` | query | `string` | no | Response format. Use json for structured records. |
