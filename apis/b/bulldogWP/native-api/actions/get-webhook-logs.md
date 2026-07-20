# Get webhook logs with Bulldog-WP

Retrieves webhook logs from Bulldog-WP.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks/{webhookId}/logs`
- **Base URL:** `https://api.bulldog-wp.co.il/v1`
- **Official documentation:** [Get webhook logs](https://console.bulldog-wp.co.il/docs/specification)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | Webhook endpoint ID. |
