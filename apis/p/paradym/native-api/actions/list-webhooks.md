# List Webhooks with Paradym

Retrieves a list of webhooks from Paradym.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/webhooks`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [List Webhooks](https://paradym.id/reference#tag/webhooks)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search[name]` | query | `string` | no | Filter webhooks by name substring. |
| `search[url]` | query | `string` | no | Filter webhooks by URL substring. |
