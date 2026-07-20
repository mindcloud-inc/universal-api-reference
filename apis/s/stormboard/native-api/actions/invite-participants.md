# Invite Participants with Stormboard

Invites participants to a Storm in Stormboard.

## Endpoint

- **Method:** `POST`
- **Path:** `/storms/:storm_id/invite`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [Invite Participants](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | no | Optional custom message to send with the invite. |
| `participants[]` | body | `array<string>` | yes | Array of email addresses to invite. |
| `storm_id` | path | `number` | yes | Storm ID from the Stormboard share dialog or related storm record. |
| `type` | body | `string` | no | Permission for invited users: contributor or viewer. |
