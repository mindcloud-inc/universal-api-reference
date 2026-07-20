# CallScaler: List Calls

Retrieves calls from CallScaler.

```
GET https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/list-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallScaler `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/list-calls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/list-calls?${params}`, {
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
| `aiCategory` | string | no |  |
| `callerName` | string | no |  |
| `callFlowId` | string | no |  |
| `direction` | string | no |  |
| `endDate` | date | no |  |
| `hasTranscription` | boolean | no |  |
| `include` | string | no |  |
| `keyword` | string | no |  |
| `maxAiScore` | number | no |  |
| `maxDuration` | number | no |  |
| `minAiScore` | number | no |  |
| `minDuration` | number | no |  |
| `numberGroupId` | string | no |  |
| `numberId` | string | no |  |
| `qualified` | boolean | no |  |
| `search` | string | no |  |
| `source` | string | no |  |
| `startDate` | date | no |  |
| `status` | string | no |  |
| `updatedSince` | date | no |  |

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
      "cost_cents": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "destination_number": "string",
      "direction": "string",
      "duration_seconds": 1,
      "has_transcription": true,
      "id": "string",
      "keywords_spotted": [
        [
          "string"
        ]
      ],
      "qualification_reason": "string",
      "qualified_ai": true,
      "recording_duration": 1,
      "recording_url": "https://example.com",
      "robo_score": 1,
      "source": "string",
      "status": "string",
      "tracking_number": "string",
      "utm_campaign": "string",
      "utm_medium": "string",
      "utm_source": "string",
      "value_cents": 1
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
| `cost_cents` | number | Call cost in cents. |
| `created_at` | date | Call creation timestamp. |
| `destination_number` | string | Forwarding destination number. |
| `direction` | string | Call direction. |
| `duration_seconds` | number | Call duration in seconds. |
| `has_transcription` | boolean | Whether transcription exists. |
| `id` | string | Unique call ID. |
| `keywords_spotted[]` | array<string> | Keywords detected in the call. |
| `qualification_reason` | string | AI qualification reason. |
| `qualified_ai` | boolean | Whether AI marked the call qualified. |
| `recording_duration` | number | Recording length in seconds. |
| `recording_url` | string | Recording URL when available. |
| `robo_score` | number | Robocall likelihood score. |
| `source` | string | Traffic source. |
| `status` | string | Call status. |
| `tracking_number` | string | CallScaler tracking number. |
| `utm_campaign` | string | UTM campaign. |
| `utm_medium` | string | UTM medium. |
| `utm_source` | string | UTM source. |
| `value_cents` | number | Assigned call value in cents. |

## Native endpoint

Through the native CallScaler API, this operation is `GET /calls` (base URL `https://callscaler.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calls.md) for the provider-specific parameters and requirements.

