# Get Board Sections with Zoho Connect

Retrieves board sections from Zoho Connect.

## Endpoint

- **Method:** `GET`
- **Path:** `/pulse/api/boardSections`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Get Board Sections](https://www.zoho.com/connect/api/get-board-sections.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boardId` | query | `string` | yes | ID of the board to return sections for. |
| `scopeID` | query | `string` | yes | ID of the network that contains the board. |
