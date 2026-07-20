# List Users with Timelink

Retrieves users from the Timelink workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [List Users](https://api.timelink.io/documentation#/Users/get_api_v1_users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search term used to match users. |
| `active` | query | `boolean` | no | Filter by active user status. |
