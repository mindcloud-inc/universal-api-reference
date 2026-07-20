# List Webhooks with Locu

Retrieves a paginated list of webhooks from Locu.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [List Webhooks](https://locu.app/api/docs#tag/webhooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isActive` | query | `string` | no | Filter by active status. Allowed values: true or false. |
