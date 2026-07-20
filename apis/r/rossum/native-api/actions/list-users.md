# List Users with Rossum

Retrieves users from Rossum.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [List Users](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter users by email address. |
| `ordering` | query | `string` | no | Ordering expression, for example email or -email. |
| `organization` | query | `string` | no | Filter users by Rossum organization URL. |
