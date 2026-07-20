# Create Group with Zoho Connect

Creates a new group in Zoho Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/pulse/api/addGroup`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Create Group](https://www.zoho.com/connect/api/create-group.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scopeID` | query | `string` | yes | Network ID. |
| `name` | query | `string` | yes | Provide a name for the group. |
| `desc` | query | `string` | no | Add a description. |
| `userIds` | query | `string<string>` | no | User IDs separated by a comma. Send multiple values as a array separated by `,`. |
| `isPrivate` | query | `boolean` | no | Set true if you want your group to be private. |
| `isOpenMembership` | query | `boolean` | no | Set true if members should find and join this group. |
| `fileId` | query | `string` | no | Add a group logo ID. |
| `createChannel` | query | `boolean` | no | Set true to create a channel for this group. |
