# Add User to a Group with Zoho Connect

Adds users to a group in Zoho Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/pulse/api/addUsersToGroup`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Add User to a Group](https://www.zoho.com/connect/api/add-user-to-group.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scopeID` | query | `string` | yes | Network ID. |
| `partitionId` | query | `string` | yes | Group ID. |
| `memberIds` | query | `string<string>` | no | User IDs separated by a comma. Send multiple values as a array separated by `,`. |
| `adminIds` | query | `string<string>` | no | Comma-separated IDs of users to add as admins. Send multiple values as a array separated by `,`. |
| `userEmailIds` | query | `string<string>` | no | Users' email addresses separated by a comma. Send multiple values as a array separated by `,`. |
