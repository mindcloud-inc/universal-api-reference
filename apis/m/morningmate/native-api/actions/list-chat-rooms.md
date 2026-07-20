# List Chat Rooms with Morningmate

Retrieves chat rooms for a Morningmate participant.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/chats/participants/[:participantId]`
- **Base URL:** `https://api.morningmate.com`
- **Official documentation:** [List Chat Rooms](https://api.morningmate.com/docs/api/v1/chats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `participantId` | path | `string` | yes | Morningmate participant user ID |
