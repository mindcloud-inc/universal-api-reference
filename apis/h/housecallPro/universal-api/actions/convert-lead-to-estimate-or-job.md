# Housecall Pro: Convert Lead to Estimate or Job



```
POST https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/convert-lead-to-estimate-or-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/convert-lead-to-estimate-or-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "type": "estimate"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/convert-lead-to-estimate-or-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "type": "estimate"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the lead to convert. |
| `type` | list | yes | Must be either estimate or job. One of: `estimate`, `job`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "estimateId": "string",
      "jobId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `estimateId` | string | Created estimate ID when the lead is converted to an estimate. |
| `jobId` | string | Created job ID when the lead is converted to a job. |

## Native endpoint

Through the native Housecall Pro API, this operation is `POST /leads/:id/convert` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-lead-to-estimate-or-job.md) for the provider-specific parameters and requirements.

