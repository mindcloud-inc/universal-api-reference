# ClearBounce: Get Batch Verification Results

Retrieves JSON batch verification results from ClearBounce.

```
GET https://connect.mindcloud.co/v1/universal/clearBounce/latest/actions/get-batch-verification-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClearBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearBounce/latest/actions/get-batch-verification-results?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearBounce/latest/actions/get-batch-verification-results?${params}`, {
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
| `jobId` | string | yes | The batch verification job ID returned by the upload step. |
| `status` | list<string> | no | Optional equality selector for a single verification status. One of: `all`, `deliverable`, `risky`, `undeliverable`, `unknown`. Default: `all`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Verification results for each processed email in the completed batch job. |
| `success` | boolean | Whether the batch results lookup succeeded. |

## Native endpoint

Through the native ClearBounce API, this operation is `GET /bulk/results/:jobId` (base URL `https://api.clearbounce.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-verification-results.md) for the provider-specific parameters and requirements.

