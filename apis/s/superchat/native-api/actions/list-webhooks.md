# List Webhooks with Superchat

Retrieves webhooks from a Superchat workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [List Webhooks](https://developers.superchat.com/reference/listwebhooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | Specify the webhook_id before which (newer) objects should be returned. |
