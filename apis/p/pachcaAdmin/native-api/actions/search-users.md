# Search Users with Pachca (Admin)

Finds users in the Pachca Admin API by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/users`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Search Users](https://dev.pachca.com/search/list-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_roles[]` | query | `array<string>` | no | Filter by company roles. |
| `created_from` | query | `date` | no | Filter users created on or after this timestamp. |
| `created_to` | query | `date` | no | Filter users created on or before this timestamp. |
| `query` | query | `string` | no | — |
| `limit` | query | `number` | no | — |
| `cursor` | query | `string` | no | — |
| `sort` | query | `string` | no | — |
| `order` | query | `string` | no | — |
