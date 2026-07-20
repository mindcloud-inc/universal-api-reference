# Invite Participants to Chat Room with Morningmate

Invites participants to a Morningmate chat room.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chats/[:roomId]/participants`
- **Base URL:** `https://api.morningmate.com`
- **Official documentation:** [Invite Participants to Chat Room](https://api.morningmate.com/docs/api/v1/chats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `number` | yes | Morningmate numeric chat room ID |
| `registerId` | body | `string` | yes | Morningmate author user ID |
| `participants[]` | body | `array<object>` | yes | Participants array |
| `participants[].participantId` | body | `string` | yes | Participant ID to invite |
