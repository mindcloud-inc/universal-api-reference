# Reorder Tour Rooms with RICOH360 Tours

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://bbomwcm27nhalfwjvwzy6qbrim.appsync-api.us-west-2.amazonaws.com`
- **Official documentation:** [Reorder Tour Rooms](https://www.ricoh360.com/tours/features/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `afterRoomId` | query | `string` | no | Room ID that should precede the moved room. |
| `roomId` | query | `string` | no | Room ID to move. |
| `tourId` | query | `string` | no | Tour ID that owns the room. |
