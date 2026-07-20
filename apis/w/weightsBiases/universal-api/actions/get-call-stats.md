# Weights & Biases: Get Call Stats

Retrieves call statistics from Weights & Biases.

```
GET https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-call-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weights & Biases `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-call-stats?connectionId=$CONNECTION_ID&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-call-stats?${params}`, {
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
| `project_id` | string | yes | W&B project identifier in entity/project format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "call_buckets": [
        {}
      ],
      "end": "2026-05-07T12:00:00.000Z",
      "granularity": 1,
      "start": "2026-05-07T12:00:00.000Z",
      "timezone": "string",
      "usage_buckets": [
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
| `call_buckets` | array<object> | Call-level metrics grouped by timestamp. |
| `end` | date | Resolved end time. |
| `granularity` | number | Bucket size used in seconds. |
| `start` | date | Resolved start time. |
| `timezone` | string | Timezone used for bucket alignment. |
| `usage_buckets` | array<object> | Usage metrics grouped by timestamp and model. |

## Native endpoint

Through the native Weights & Biases API, this operation is `POST /calls/stats` (base URL `https://trace.wandb.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-stats.md) for the provider-specific parameters and requirements.

