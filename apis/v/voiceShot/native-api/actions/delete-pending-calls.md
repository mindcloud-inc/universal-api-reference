# Delete Pending Calls with VoiceShot

Deletes pending calls from a VoiceShot campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/ivrapi.asp`
- **Base URL:** `https://api.voiceshot.com`
- **Official documentation:** [Delete Pending Calls](https://secure.voiceshot.com/docs/ivrapiv5/action.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `menuId` | body | `string` | yes | VoiceShot campaign identifier. |
| `callIds[]` | body | `array<string>` | yes | Call identifiers to remove from the pending queue. |
