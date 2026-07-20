# Update Media Speakers with Speak Ai

Updates transcript speaker names in Speak Ai.

## Endpoint

- **Method:** `PUT`
- **Path:** `/media/speakers/:mediaId`
- **Base URL:** `https://api.speakai.co/v1`
- **Official documentation:** [Update Media Speakers](https://docs.speakai.co/#eacfa313-5bb9-47b7-ad8b-ae730b89de5a)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mediaId` | path | `string` | yes | Speak Ai media identifier. |
| `speakersJson` | body | `string` | yes | JSON array of speaker objects like [{"id":"0","name":"Speaker 1"}] to send as the root request body. |
