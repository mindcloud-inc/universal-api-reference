# List Users with Qlik

Retrieves users from your Qlik tenant.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/users`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [List Users](https://qlik.dev/apis/rest/users/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Optional SCIM filter expression. |
