# Create Board with Zoho Connect

Creates a new board in Zoho Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/pulse/api/addBoard`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Create Board](https://www.zoho.com/connect/api/create-board.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `desc` | query | `string` | yes | Description for the board. |
| `memberIds` | query | `string` | no | Comma-separated Zoho user IDs to add to the board. Send multiple values as a string separated by `,`. |
| `name` | query | `string` | yes | Name of the board to create. |
| `scopeID` | query | `string` | yes | ID of the network where the board will be created. |
