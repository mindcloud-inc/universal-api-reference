# List Subscriptions with Signaturit

Retrieves subscriptions from Signaturit.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscriptions.json`
- **Base URL:** `https://api.sandbox.signaturit.com/v3`
- **API:** rest
- **Official documentation:** [List Subscriptions](https://docs.signaturit.com/api/latest#subscriptions_get_subscriptions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | query | `string` | no | Filter subscriptions attached to a specific event. |
