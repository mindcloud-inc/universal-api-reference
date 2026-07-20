# List Users with LimoExpress

Retrieves users from the LimoExpress organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integration/users`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [List Users](https://api.limoexpress.me/api/docs/v1#/Users/getAllUsers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_string` | query | `string` | no | Search across user fields. |
| `page` | query | `number` | no | Page number, default is 1. |
| `per_page` | query | `number` | no | Items per page, default is 20. |
