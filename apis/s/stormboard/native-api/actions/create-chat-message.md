# Create Chat Message with Stormboard

Creates a chat message in Stormboard.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/:storm_id`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [Create Chat Message](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Chat message text to post in the storm. |
| `storm_id` | path | `number` | yes | Storm ID from the Stormboard share dialog or related storm record. |
