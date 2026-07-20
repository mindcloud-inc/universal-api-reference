# List Users with RapidAPI

Retrieves users from RapidAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/users`
- **Base URL:** `{baseUrlRest}`
- **Official documentation:** [List Users](https://docs.rapidapi.com/docs/on-behalf-of)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter users by email address. |
| `limit` | query | `number` | no | Maximum number of users to return. |
