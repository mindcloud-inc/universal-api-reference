# Orq.ai: Create Transcription

Creates an audio transcription in Orq.ai.

```
GET https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-transcription?connectionId=$CONNECTION_ID&file=string&model=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "string",
  "model": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-transcription?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes |  |
| `model` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "text": "string",
      "usage": {
        "seconds": 1,
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `text` | string |  |
| `usage.seconds` | number |  |
| `usage.type` | string |  |

## Native endpoint

Through the native Orq.ai API, this operation is `POST /v2/router/audio/transcriptions` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transcription.md) for the provider-specific parameters and requirements.

