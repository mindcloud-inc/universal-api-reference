# Simpro: Update Job



```
PUT https://connect.mindcloud.co/v1/universal/simpro/latest/actions/update-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/update-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "0",
  "jobId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpro/latest/actions/update-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "0",
    "jobId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Default: `0`. |
| `jobId` | number | yes |  |
| `Description` | string | no |  |
| `Notes` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Simpro API returns.

## Native endpoint

Through the native Simpro API, this operation is `PATCH /companies/:companyId/jobs/:jobId` (base URL `https://mindcloud.simprosuite.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job.md) for the provider-specific parameters and requirements.

