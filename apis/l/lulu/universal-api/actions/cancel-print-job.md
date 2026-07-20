# Lulu: Cancel Print Job

Cancels a print job in Lulu.

```
DELETE https://connect.mindcloud.co/v1/universal/lulu/latest/actions/cancel-print-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/cancel-print-job?connectionId=$CONNECTION_ID&id=job_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "job_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lulu/latest/actions/cancel-print-job?${params}`, {
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
| `id` | string | yes | Lulu print job ID. Default: `job_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changed": "string",
      "message": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changed` | string |  |
| `message` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Lulu API, this operation is `PUT /print-jobs/{id}/status/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-print-job.md) for the provider-specific parameters and requirements.

