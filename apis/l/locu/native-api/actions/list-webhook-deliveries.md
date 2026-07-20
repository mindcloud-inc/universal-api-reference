# List Webhook Deliveries with Locu

Retrieves recent webhook deliveries from Locu.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks/:id/deliveries`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [List Webhook Deliveries](https://locu.app/api/docs#tag/webhooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Webhook ID to list deliveries for. |
