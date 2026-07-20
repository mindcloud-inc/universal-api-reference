# NeverBounce: Delete Job

Deletes an existing verification job from NeverBounce.

```
DELETE https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/delete-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeverBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/delete-job?connectionId=$CONNECTION_ID&jobId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/delete-job?${params}`, {
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
| `jobId` | number | yes | NeverBounce job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionTime": 1,
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
| `status` | string |  |

## Native endpoint

Through the native NeverBounce API, this operation is `POST /jobs/delete` (base URL `https://api.neverbounce.com/v4.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-job.md) for the provider-specific parameters and requirements.

