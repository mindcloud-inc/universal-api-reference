# List Events with Eventzilla

Retrieves events from Eventzilla.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://www.eventzillaapi.net/api/v2`
- **Official documentation:** [List Events](https://developer.eventzilla.net/docs/#events)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter events by Eventzilla status such as live or completed. |
| `category` | query | `string` | no | Filter events by category. |
