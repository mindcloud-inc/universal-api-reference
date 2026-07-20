# PiAPI/DiffRhythm: Generate Audio

Creates a DiffRhythm audio task in PiAPI/DiffRhythm.

```
POST https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/generate-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/DiffRhythm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/generate-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskType": "txt2audio-base",
  "input.lyrics": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/generate-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskType": "txt2audio-base",
    "input.lyrics": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskType` | string | yes | Choose `txt2audio-base` for shorter generations or `txt2audio-full` for longer songs. Default: `txt2audio-base`. |
| `input.lyrics` | string | yes | Timed lyrics in DiffRhythm format such as `[00:10.00] line of lyrics`. |
| `input.stylePrompt` | string | no | Describe the musical style, genre, or mood when you are not using a reference audio file. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.styleAudio` | string | no | Optional reference audio URL or Base64 string to guide the generated style. |
| `config.webhookConfig.endpoint` | string | no | Optional webhook URL for PiAPI task completion callbacks. |
| `config.webhookConfig.secret` | string | no | Optional secret that PiAPI includes when calling your webhook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {
        "serviceMode": "string",
        "webhookConfig": {
          "endpoint": "string",
          "secret": "string"
        }
      },
      "detail": {},
      "error": {
        "code": 1,
        "detail": {},
        "message": "string",
        "rawMessage": "string"
      },
      "input": {
        "lyrics": "string",
        "styleAudio": "string",
        "stylePrompt": "string"
      },
      "logs": [
        {}
      ],
      "meta": {
        "createdAt": "string",
        "endedAt": "string",
        "isUsingPrivatePool": true,
        "startedAt": "string",
        "usage": {
          "consume": 1,
          "frozen": 1,
          "type": "string"
        }
      },
      "model": "string",
      "output": {},
      "status": "string",
      "taskId": "string",
      "taskType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config.serviceMode` | string |  |
| `config.webhookConfig.endpoint` | string |  |
| `config.webhookConfig.secret` | string |  |
| `detail` | object |  |
| `error.code` | number |  |
| `error.detail` | object |  |
| `error.message` | string |  |
| `error.rawMessage` | string |  |
| `input.lyrics` | string |  |
| `input.styleAudio` | string |  |
| `input.stylePrompt` | string |  |
| `logs` | array<object> |  |
| `meta.createdAt` | string |  |
| `meta.endedAt` | string |  |
| `meta.isUsingPrivatePool` | boolean |  |
| `meta.startedAt` | string |  |
| `meta.usage.consume` | number |  |
| `meta.usage.frozen` | number |  |
| `meta.usage.type` | string |  |
| `model` | string |  |
| `output` | object |  |
| `status` | string |  |
| `taskId` | string |  |
| `taskType` | string |  |

## Native endpoint

Through the native PiAPI/DiffRhythm API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-audio.md) for the provider-specific parameters and requirements.

