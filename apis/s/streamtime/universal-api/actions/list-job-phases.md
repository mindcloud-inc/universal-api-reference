# Streamtime: List Job Phases



```
GET https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-job-phases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-job-phases?connectionId=$CONNECTION_ID&jobId=601" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "601"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-job-phases?${params}`, {
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
| `jobId` | number | yes | Job ID Example: `601`. |

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
| `jobId` | number | Job ID |
| `name` | string | Job phase name |
| `orderId` | number | Job phase order |

## Native endpoint

Through the native Streamtime API, this operation is `GET /jobs/:job_id/job_phases` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-phases.md) for the provider-specific parameters and requirements.

