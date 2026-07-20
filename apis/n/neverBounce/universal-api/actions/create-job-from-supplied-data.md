# NeverBounce: Create Job From Supplied Data

Creates a verification job in NeverBounce from supplied rows.

```
POST https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/create-job-from-supplied-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeverBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/create-job-from-supplied-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input[]": [
    {}
  ],
  "input[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/create-job-from-supplied-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input[]": [{}],
    "input[].email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input[]` | array<object> | yes | Supplied rows to verify. |
| `input[].email` | string | yes | Email address for the supplied row. |
| `input[].name` | string | no | Optional name or label to store with the supplied row. |
| `autoParse` | boolean | no | Parse the job immediately after creation. |
| `autoStart` | boolean | no | Start the job immediately after it is parsed. |
| `runSample` | boolean | no | Run the provider sample mode before processing the full job. |
| `fileName` | string | no | Display filename for the supplied job. |
| `allowManualReview` | boolean | no | Allow manual review for unresolved rows. |
| `callbackUrl` | string | no | Webhook URL for job updates. |
| `callbackHeaders` | object | no | Optional headers to send with the callback request. |
| `leverageHistoricalData` | number | no | Set to 1 to enable NeverBounce historical-data leverage for this job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionTime": 1,
      "jobId": 1,
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
| `jobId` | number |  |
| `status` | string |  |

## Native endpoint

Through the native NeverBounce API, this operation is `POST /jobs/create` (base URL `https://api.neverbounce.com/v4.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job-from-supplied-data.md) for the provider-specific parameters and requirements.

