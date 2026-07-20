# List Tickets with Donorbox

Retrieves tickets from Donorbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets`
- **Base URL:** `https://donorbox.org/api/v1`
- **Official documentation:** [List Tickets](https://github.com/donorbox/donorbox-api#tickets)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payment_status` | query | `string` | no | Filter tickets by payment status (for example refunded). |
