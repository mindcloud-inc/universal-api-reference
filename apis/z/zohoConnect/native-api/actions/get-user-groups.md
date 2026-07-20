# Get User Groups with Zoho Connect

Retrieves a user's groups from Zoho Connect.

## Endpoint

- **Method:** `GET`
- **Path:** `/pulse/api/userGroups`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Get User Groups](https://www.zoho.com/connect/api/get-user-groups.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scopeID` | query | `string` | yes | Network ID. |
| `isRecentSort` | query | `boolean` | yes | Sort groups by recency. |
