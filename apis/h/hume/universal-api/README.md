# <img src="https://images.mindcloud.co/apps/icons/favicon-dev-hume-ai-48x48_1777484824019.png" alt="Hume logo" width="28" height="28"> Hume: Universal API

Hume provides emotionally intelligent voice AI APIs for speech-to-speech conversations, expressive text-to-speech, custom voices, and expression measurement.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hume/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hume.ai
- **Vendor API docs:** https://dev.hume.ai/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get chat audio](actions/get-chat-audio.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hume/latest/actions/get-chat-audio?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Chat Audio

| Action | Method | Description |
| --- | --- | --- |
| [Get chat audio](actions/get-chat-audio.md) | GET |  |

### Chat Event

| Action | Method | Description |
| --- | --- | --- |
| [List chat events](actions/list-chat-events.md) | GET |  |

### Chat Group Audio

| Action | Method | Description |
| --- | --- | --- |
| [Get chat group audio](actions/get-chat-group-audio.md) | GET |  |

### Chat Group Event

| Action | Method | Description |
| --- | --- | --- |
| [List chat group events](actions/list-chat-group-events.md) | GET |  |

### Evi Chat

| Action | Method | Description |
| --- | --- | --- |
| [List chats](actions/list-chats.md) | GET |  |

### Evi Chat Group

| Action | Method | Description |
| --- | --- | --- |
| [Get chat group](actions/get-chat-group.md) | GET |  |
| [List chat groups](actions/list-chat-groups.md) | GET |  |

### Evi Config

| Action | Method | Description |
| --- | --- | --- |
| [Create config](actions/create-config.md) | POST |  |
| [Delete config](actions/delete-config.md) | DELETE |  |
| [List configs](actions/list-configs.md) | GET |  |
| [Update config name](actions/update-config-name.md) | PUT |  |

### Evi Config Version

| Action | Method | Description |
| --- | --- | --- |
| [Create config version](actions/create-config-version.md) | POST |  |
| [Delete config version](actions/delete-config-version.md) | DELETE |  |
| [Get config version](actions/get-config-version.md) | GET |  |
| [List config versions](actions/list-config-versions.md) | GET |  |
| [Update config description](actions/update-config-description.md) | PUT |  |

### Evi Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Create prompt](actions/create-prompt.md) | POST |  |
| [Delete prompt](actions/delete-prompt.md) | DELETE |  |
| [List prompts](actions/list-prompts.md) | GET |  |
| [Update prompt name](actions/update-prompt-name.md) | PUT |  |

### Evi Prompt Version

| Action | Method | Description |
| --- | --- | --- |
| [Create prompt version](actions/create-prompt-version.md) | POST |  |
| [Delete prompt version](actions/delete-prompt-version.md) | DELETE |  |
| [Get prompt version](actions/get-prompt-version.md) | GET |  |
| [List prompt versions](actions/list-prompt-versions.md) | GET |  |
| [Update prompt description](actions/update-prompt-description.md) | PUT |  |

### Evi Tool

| Action | Method | Description |
| --- | --- | --- |
| [Create tool](actions/create-tool.md) | POST |  |
| [Delete tool](actions/delete-tool.md) | DELETE |  |
| [List tools](actions/list-tools.md) | GET |  |
| [Update tool name](actions/update-tool-name.md) | PUT |  |

### Evi Tool Version

| Action | Method | Description |
| --- | --- | --- |
| [Create tool version](actions/create-tool-version.md) | POST |  |
| [Delete tool version](actions/delete-tool-version.md) | DELETE |  |
| [Get tool version](actions/get-tool-version.md) | GET |  |
| [List tool versions](actions/list-tool-versions.md) | GET |  |
| [Update tool description](actions/update-tool-description.md) | PUT |  |

### Expression Measurement Job

| Action | Method | Description |
| --- | --- | --- |
| [Get job details](actions/get-job-details.md) | GET |  |
| [List jobs](actions/list-jobs.md) | GET |  |

### Job Artifact

| Action | Method | Description |
| --- | --- | --- |
| [Get job artifacts](actions/get-job-artifacts.md) | GET |  |

### Job Prediction

| Action | Method | Description |
| --- | --- | --- |
| [Get job predictions](actions/get-job-predictions.md) | GET |  |

### Speech Generation

| Action | Method | Description |
| --- | --- | --- |
| [Synthesize speech](actions/synthesize-speech.md) | POST |  |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [List voices](actions/list-voices.md) | GET |  |

