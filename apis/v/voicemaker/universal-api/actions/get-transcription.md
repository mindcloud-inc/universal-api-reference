# Voicemaker: Get Transcription

Retrieves a single transcription from Voicemaker.

```
GET https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/get-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voicemaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/get-transcription?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/get-transcription?${params}`, {
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
| `taskId` | string | yes | Transcription task ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {}
      ],
      "limit": "string",
      "page": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data` | array<object> |  |
| `limit` | string |  |
| `page` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Voicemaker API, this operation is `GET api/v1/speech-to-text/{taskId}` (base URL `https://developer.voicemaker.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcription.md) for the provider-specific parameters and requirements.

