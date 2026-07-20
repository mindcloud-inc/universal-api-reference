# Instant Voice Clone with Uberduck

Creates a zero-shot voice in Uberduck.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/voices`
- **Base URL:** `https://api.uberduck.ai`
- **Official documentation:** [Instant Voice Clone](https://docs.uberduck.ai/api-reference/instant-voice-clone-v-1-voices-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for the new zero-shot voice clone. |
| `paths` | body | `list<string>` | yes | List of source audio URLs Uberduck should use for cloning. Send multiple values as a array. |
