# List Deals with Paycove

Retrieves deals from Paycove.

## Endpoint

- **Method:** `GET`
- **Path:** `deals`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [List Deals](https://docs.paycove.io/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_field_keys[]` | query | `array<string>` | no | Array of custom field keys to include in the response. |
| `include_payments` | query | `boolean` | no | Include nested payments in the response. |
