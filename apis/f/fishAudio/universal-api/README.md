# <img src="https://images.mindcloud.co/apps/icons/images-15_1775842880367.png" alt="Fish Audio logo" width="28" height="28"> Fish Audio: Universal API

Fish Audio is an AI voice generation platform for text-to-speech, speech-to-text, and custom voice model management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fishAudio/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fish.audio
- **Vendor API docs:** https://docs.fish.audio/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Credit](actions/get-api-credit.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/get-api-credit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Create Model](actions/create-model.md) | POST | Creates a new voice model in Fish Audio. |
| [Delete Model](actions/delete-model.md) | DELETE | Deletes an existing voice model from Fish Audio. |
| [Get Model](actions/get-model.md) | GET | Finds a voice model in Fish Audio by ID. |
| [List Models](actions/list-models.md) | GET | Retrieves voice models from Fish Audio. |
| [Update Model](actions/update-model.md) | PUT | Updates an existing voice model in Fish Audio. |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [Speech to Text](actions/speech-to-text.md) | POST | Transcribes audio to text with Fish Audio. |
| [Text to Speech](actions/text-to-speech.md) | POST | Converts text to speech with Fish Audio. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Get API Credit](actions/get-api-credit.md) | GET | Retrieves current API credit balance from Fish Audio. |
| [Get User Package](actions/get-user-package.md) | GET | Retrieves current user package details from Fish Audio. |

