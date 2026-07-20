# Get All Groups with Zoho Connect

Retrieves all groups from Zoho Connect.

## Endpoint

- **Method:** `GET`
- **Path:** `/pulse/api/allGroups`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Get All Groups](https://www.zoho.com/connect/api/get-all-groups.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scopeID` | query | `string` | yes | Network ID. |
| `isRecentSort` | query | `boolean` | no | Sort groups by recency. |
