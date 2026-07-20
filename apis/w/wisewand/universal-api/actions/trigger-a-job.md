# Wisewand: Trigger a job

Triggers a job in your Wisewand workspace.

```
POST https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/trigger-a-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/trigger-a-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "daily-sync"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/trigger-a-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "daily-sync"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The job name (e.g., generate-image) Default: `daily-sync`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "step": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The job ID |
| `name` | string | The job name |
| `status` | string | The job status |
| `step` | string | The job step |

## Native endpoint

Through the native Wisewand API, this operation is `POST /v1/jobs/:name` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-a-job.md) for the provider-specific parameters and requirements.

