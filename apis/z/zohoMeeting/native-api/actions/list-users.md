# List Users with Zoho Meeting

Retrieves users from Zoho Meeting.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:organizationId/user`
- **Base URL:** `https://meeting.zoho.com`
- **Official documentation:** [List Users](https://www.zoho.com/meeting/api-integration/user-api/list-of-users.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID (zsoid) from Get Current User Details. |
