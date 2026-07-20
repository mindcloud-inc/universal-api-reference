# <img src="https://images.mindcloud.co/apps/icons/icon-1_1776706148368.png" alt="LMNT logo" width="28" height="28"> LMNT: Universal API

Generate low-latency AI speech, voice clones, and real-time text-to-speech with LMNT.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lMNT/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lmnt.com
- **Vendor API docs:** https://docs.lmnt.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Account Info](actions/account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Account Info](actions/account-info.md) | GET | Retrieves your account details from LMNT. |

### Speech

| Action | Method | Description |
| --- | --- | --- |
| [Generate Speech (Bytes)](actions/generate-speech-bytes.md) | POST | Creates streaming speech audio from text in LMNT. |
| [Generate Speech (Detailed)](actions/generate-speech-detailed.md) | POST | Creates timestamped speech output from text in LMNT. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [Create Voice](actions/create-voice.md) | POST | Creates a new voice in LMNT. |
| [Delete Voice](actions/delete-voice.md) | DELETE | Deletes an existing voice from LMNT. |
| [List Voices](actions/list-voices.md) | GET | Retrieves a list of available voices from LMNT. |
| [Update Voice](actions/update-voice.md) | PUT | Updates an existing voice in LMNT. |
| [Voice Info](actions/voice-info.md) | GET | Retrieves details for a specific voice from LMNT. |

