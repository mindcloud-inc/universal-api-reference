# WhatsScale: Check Job Status

Retrieves an async job status from WhatsScale.

```
GET https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/check-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsScale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/check-job-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/check-job-status?${params}`, {
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
| `jobId` | string | yes | Job ID returned by async send or story endpoints. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "string",
      "createdAt": "string",
      "error": "string",
      "result": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | string |  |
| `createdAt` | string |  |
| `error` | string |  |
| `result` | object |  |
| `status` | string |  |

## Native endpoint

Through the native WhatsScale API, this operation is `GET /api/status/:jobId` (base URL `https://proxy.whatsscale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-job-status.md) for the provider-specific parameters and requirements.

