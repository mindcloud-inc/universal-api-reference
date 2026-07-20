# Search Users with Timely

Finds users in Timely.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.1/{account_id}/users/search`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Search Users](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Workspace id |
| `q` | query | `string` | yes | Search query |
