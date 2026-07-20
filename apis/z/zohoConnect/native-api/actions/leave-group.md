# Leave Group with Zoho Connect

Leaves a group in Zoho Connect.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/pulse/api/leaveGroup`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Leave Group](https://www.zoho.com/connect/api/leave-group.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scopeID` | query | `string` | yes | Network ID. |
| `partitionId` | query | `string` | yes | Group ID. |
