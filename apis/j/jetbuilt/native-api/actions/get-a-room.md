# Get a Room with Jetbuilt

Retrieve the details of an individual project room. Equipment and labor totals (cost & price). Line items in this room. Project factors, along with how much of each factor applies to the room.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:projectId/rooms/:roomId`
- **Base URL:** `https://app.jetbuilt.com/api/`
- **Official documentation:** [Get a Room](https://api.jetbuilt.com/customers?shell--json#get-a-room-in-your-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | — |
| `roomId` | path | `string` | yes | The Id of the Room to retrieve details for. To get a room ID, use the "Get All Rooms" Action to find the RoomId 's available for a given project. |
