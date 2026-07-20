# Create Deals Batch with BoardCRM

Creates multiple deal records in BoardCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/offer/create-some`
- **Base URL:** `https://api.boardcrm.io/api`
- **Official documentation:** [Create Deals Batch](https://dev.boardcrm.io/public/0.1/methods/offer#create-some)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offers[]` | body | `array<object>` | yes | Array of deal payloads using the BoardCRM create-deal shape. |
