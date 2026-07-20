# NeverBounce: Parse Job

Updates an existing NeverBounce job by parsing its uploaded data.

```
PUT https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/parse-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeverBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/parse-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/parse-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | number | yes | NeverBounce job identifier. |
| `autoStart` | boolean | no | Start the job automatically after parsing completes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionTime": 1,
      "queueId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `executionTime` | number |  |
| `queueId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native NeverBounce API, this operation is `POST /jobs/parse` (base URL `https://api.neverbounce.com/v4.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-job.md) for the provider-specific parameters and requirements.

