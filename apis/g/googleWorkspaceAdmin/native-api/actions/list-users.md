# List Users with Google Workspace Admin

Retrieves users from Google Workspace Admin.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/directory/v1/users`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [List Users](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | query | `string` | yes | Workspace customer identifier. Keep `my_customer` for the current tenant unless you need a specific customer ID. |
| `maxResults` | query | `number` | no | Maximum users to return (up to 500). |
| `pageToken` | query | `string` | no | Pagination token from previous response. |
