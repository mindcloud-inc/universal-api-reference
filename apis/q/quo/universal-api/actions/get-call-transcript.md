# Quo: Get Call Transcript

Retrieves a transcription for a Quo call.

```
GET https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-call-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-call-transcript?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-call-transcript?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dialogue": [
        {}
      ],
      "duration": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callId` | string |  |
| `createdAt` | date |  |
| `dialogue` | array<object> |  |
| `duration` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Quo API, this operation is `GET /call-transcripts/:id` (base URL `https://api.openphone.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-transcript.md) for the provider-specific parameters and requirements.

