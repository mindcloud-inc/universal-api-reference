# Create Channel with Are.na

Creates a new channel in Are.na.

## Endpoint

- **Method:** `POST`
- **Path:** `channels`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [Create Channel](https://www.are.na/developers/explore/channel/post-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Channel description in markdown. |
| `title` | body | `string` | no | Channel title. |
| `visibility` | body | `string` | no | Channel visibility: public, closed, or private. |
