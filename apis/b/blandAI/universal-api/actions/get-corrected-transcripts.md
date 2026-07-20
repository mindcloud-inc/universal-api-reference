# Bland AI: Get Corrected Transcripts

Retrieves corrected transcripts for a call in Bland AI.

```
GET https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/get-corrected-transcripts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bland AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/get-corrected-transcripts?connectionId=$CONNECTION_ID&callId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "callId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/get-corrected-transcripts?${params}`, {
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
| `callId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aligned": [
        {}
      ],
      "corrected": [
        {}
      ],
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aligned` | array<object> |  |
| `corrected` | array<object> |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bland AI API, this operation is `GET /v1/calls/{call_id}/correct` (base URL `https://api.bland.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-corrected-transcripts.md) for the provider-specific parameters and requirements.

