# List Spaces with Qlik

Retrieves spaces from your Qlik tenant.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/spaces`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [List Spaces](https://qlik.dev/apis/rest/spaces/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Optional space name filter. |
| `type` | query | `string` | no | Optional space type filter. |
