# CallScaler: Batch Lookup Calls

Finds calls in CallScaler by batch lookup.

```
GET https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/batch-lookup-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallScaler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/batch-lookup-calls?connectionId=$CONNECTION_ID&ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/batch-lookup-calls?${params}`, {
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
| `ids[]` | array<string> | yes | Up to 100 call IDs to retrieve. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ai_category": "string",
      "ai_score": 1,
      "call_flow_name": "Ava Chen",
      "caller_name": "Ava Chen",
      "caller_number": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "destination_number": "string",
      "direction": "string",
      "duration_seconds": 1,
      "has_transcription": true,
      "id": "string",
      "qualified_ai": true,
      "recording_url": "https://example.com",
      "source": "string",
      "status": "string",
      "tracking_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai_category` | string | AI category. |
| `ai_score` | number | AI quality score. |
| `call_flow_name` | string | Call flow name. |
| `caller_name` | string | Caller name. |
| `caller_number` | string | Caller phone number. |
| `created_at` | date | Call creation timestamp. |
| `destination_number` | string | Forwarding destination number. |
| `direction` | string | Call direction. |
| `duration_seconds` | number | Call duration in seconds. |
| `has_transcription` | boolean | Whether transcription exists. |
| `id` | string | Unique call ID. |
| `qualified_ai` | boolean | Whether AI marked the call qualified. |
| `recording_url` | string | Recording URL when available. |
| `source` | string | Traffic source. |
| `status` | string | Call status. |
| `tracking_number` | string | CallScaler tracking number. |

## Native endpoint

Through the native CallScaler API, this operation is `POST /calls/batch` (base URL `https://callscaler.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-lookup-calls.md) for the provider-specific parameters and requirements.

