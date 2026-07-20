# Lulu: Get Print Job Status

Retrieves the status of a print job from Lulu.

```
GET https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-print-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-print-job-status?connectionId=$CONNECTION_ID&id=job_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "job_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-print-job-status?${params}`, {
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

Through the native Lulu API, this operation is `GET /print-jobs/{id}/status/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-print-job-status.md) for the provider-specific parameters and requirements.

