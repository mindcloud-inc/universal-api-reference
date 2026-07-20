# Add Member to a Board with Zoho Connect

Adds members to a board in Zoho Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/pulse/api/addMembersToBoard`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Add Member to a Board](https://www.zoho.com/connect/api/add-member-to-board.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boardId` | query | `string` | yes | ID of the board to add members to. |
| `memberIds` | query | `string` | yes | Comma-separated user IDs to add to the board. Send multiple values as a string separated by `,`. |
| `scopeID` | query | `string` | yes | ID of the network that contains the board. |
