# List Users with Timely

Retrieves users from Timely.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.1/{account_id}/users`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [List Users](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Workspace id |
| `limit` | query | `number` | no | Maximum number of results to return |
| `offset` | query | `number` | no | Number of results to skip |
| `order` | query | `string` | no | Sort order |
| `filter` | query | `string` | no | Filter for deleted users |
