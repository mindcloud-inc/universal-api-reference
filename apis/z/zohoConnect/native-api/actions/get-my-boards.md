# Get My Boards with Zoho Connect

Retrieves your boards from Zoho Connect.

## Endpoint

- **Method:** `GET`
- **Path:** `/pulse/api/myBoards`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Get My Boards](https://www.zoho.com/connect/api/get-my-boards.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boardsModifiedTime` | query | `number` | no | Fetch boards modified after this Unix timestamp in milliseconds. |
| `scopeID` | query | `string` | yes | ID of the network to fetch boards from. |
