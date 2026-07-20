# List Purchases with Donorbox

Retrieves event ticket purchases from Donorbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/purchases`
- **Base URL:** `https://donorbox.org/api/v1`
- **Official documentation:** [List Purchases](https://github.com/donorbox/donorbox-api#event-ticket-purchases)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payment_status` | query | `string` | no | Filter purchases by payment status (for example refunded). |
