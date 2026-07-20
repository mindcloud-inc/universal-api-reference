# Bland AI: Call Details

Retrieves call details from your Bland AI account.

```
GET https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/call-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bland AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/call-details?connectionId=$CONNECTION_ID&callId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "callId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/call-details?${params}`, {
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
      "analysis": {},
      "call_id": "string",
      "citations": [
        {}
      ],
      "completed": true,
      "created_at": "string",
      "pathway_id": "string",
      "price": 1,
      "queue_status": "string",
      "recording_url": "https://example.com",
      "summary": "string",
      "transcripts": [
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
| `analysis` | object |  |
| `call_id` | string |  |
| `citations` | array<object> |  |
| `completed` | boolean |  |
| `created_at` | string |  |
| `pathway_id` | string |  |
| `price` | number |  |
| `queue_status` | string |  |
| `recording_url` | string |  |
| `summary` | string |  |
| `transcripts` | array<object> |  |

## Native endpoint

Through the native Bland AI API, this operation is `GET /v1/calls/{call_id}` (base URL `https://api.bland.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/call-details.md) for the provider-specific parameters and requirements.

