# Send Message to Chat Room with Morningmate

Creates a message in a Morningmate chat room.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chats/[:roomId]/messages`
- **Base URL:** `https://api.morningmate.com`
- **Official documentation:** [Send Message to Chat Room](https://api.morningmate.com/docs/api/v1/chats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `number` | yes | Morningmate numeric chat room ID |
| `registerId` | body | `string` | yes | Morningmate author user ID |
| `contents` | body | `string` | yes | Message body |
