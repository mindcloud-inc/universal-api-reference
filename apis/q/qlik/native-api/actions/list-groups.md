# List Groups with Qlik

Retrieves groups from your Qlik tenant.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/groups`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [List Groups](https://qlik.dev/apis/rest/groups/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Optional SCIM filter expression. |
