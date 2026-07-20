# Query Call By Call ID with VoiceShot

Retrieves a call from VoiceShot by call ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/ivrapi.asp`
- **Base URL:** `https://api.voiceshot.com`
- **Official documentation:** [Query Call By Call ID](https://secure.voiceshot.com/docs/ivrapiv5/callquery.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `menuId` | body | `string` | yes | VoiceShot campaign identifier. |
| `callId` | body | `string` | yes | Call identifier to query. |
