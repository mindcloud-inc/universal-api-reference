# Celigo: Cancel Job



```
PUT https://connect.mindcloud.co/v1/universal/celigo/latest/actions/cancel-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/cancel-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "6798e7a330f8f5fb4c2ee2fb"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/celigo/latest/actions/cancel-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "6798e7a330f8f5fb4c2ee2fb"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | string | yes | Parent flow-run job to cancel. Only queued, running or retrying jobs can be canceled. Example: `6798e7a330f8f5fb4c2ee2fb`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Celigo API returns.

## Native endpoint

Through the native Celigo API, this operation is `PUT /jobs/:jobId/cancel` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-job.md) for the provider-specific parameters and requirements.

