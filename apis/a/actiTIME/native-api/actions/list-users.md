# List Users with actiTIME

Retrieves a list of users from actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Users](https://www.actitime.com/api-documentation/users-resource)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `boolean` | no | Filter active vs inactive users. |
| `department` | query | `string` | no | — |
| `email` | query | `string` | no | — |
| `ids` | query | `string` | no | — |
| `includeReferenced` | query | `string` | no | — |
| `name` | query | `string` | no | — |
| `sort` | query | `string` | no | Sorting tokens like +lastName or -hired. |
| `timeZoneGroup` | query | `string` | no | — |
| `username` | query | `string` | no | — |
