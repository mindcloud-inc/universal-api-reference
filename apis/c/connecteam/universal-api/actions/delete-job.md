# Connecteam: Delete Job

Delete a single job by its unique identifier.
        Currently, deleting a sub-job and/or job with nested sub-jobs is not supported.

```
DELETE https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/delete-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/delete-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/delete-job?${params}`, {
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
| `jobId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `requestId` | string |  |

## Native endpoint

Through the native Connecteam API, this operation is `DELETE /jobs/v1/jobs/:jobId` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-job.md) for the provider-specific parameters and requirements.

