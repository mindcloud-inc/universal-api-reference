# Soniox: Get transcription transcript

Retrieves transcript text for a Soniox transcription.

```
GET https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-transcription-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soniox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-transcription-transcript?connectionId=$CONNECTION_ID&transcriptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transcriptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-transcription-transcript?${params}`, {
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
| `transcriptionId` | string | yes | Unique identifier of the transcription. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "text": "string",
      "tokens": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Transcription identifier. |
| `text` | string | Complete transcript text. |
| `tokens` | array<object> | Detailed transcript tokens with timestamps. |

## Native endpoint

Through the native Soniox API, this operation is `GET /transcriptions/:transcription_id/transcript` (base URL `https://api.soniox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcription-transcript.md) for the provider-specific parameters and requirements.

