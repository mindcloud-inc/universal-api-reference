# NeverBounce: Create Job From Remote URL

Creates a verification job in NeverBounce from a remote CSV URL.

```
POST https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/create-job-from-remote-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeverBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/create-job-from-remote-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "remoteUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/create-job-from-remote-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "remoteUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `autoParse` | boolean | no | Parse the job automatically after creation. |
| `remoteUrl` | string | yes | Remote CSV URL for NeverBounce to import. |
| `autoStart` | boolean | no | Start the job automatically after parsing completes. |
| `runSample` | boolean | no | Run the sample flow before processing the full job. |
| `fileName` | string | no | Filename to associate with the job. |
| `allowManualReview` | boolean | no | Allow NeverBounce manual review for this job. |
| `callbackUrl` | string | no | Webhook URL NeverBounce should call after job events. |
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

Through the native NeverBounce API, this operation is `POST /jobs/create` (base URL `https://api.neverbounce.com/v4.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job-from-remote-url.md) for the provider-specific parameters and requirements.

