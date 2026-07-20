# Streamtime: Create Job Phase



```
POST https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-job-phase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-job-phase" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "601",
  "name": "Initial Scoping"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-job-phase', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "601",
    "name": "Initial Scoping"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | number | yes | Job ID Example: `601`. |
| `name` | string | yes | Name of the phase Example: `Initial Scoping`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "jobId": 1,
      "name": "Ava Chen",
      "orderId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Job phase ID |
| `jobId` | number | Parent job ID |
| `name` | string | Phase name |
| `orderId` | number | Phase order |

## Native endpoint

Through the native Streamtime API, this operation is `POST /jobs/:job_id/job_phases` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job-phase.md) for the provider-specific parameters and requirements.

