# Hume: Get job details



```
GET https://connect.mindcloud.co/v1/universal/hume/latest/actions/get-job-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hume/latest/actions/get-job-details?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hume/latest/actions/get-job-details?${params}`, {
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
| `id` | string | yes | Expression Measurement job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedTimestampMs": 1,
      "createdTimestampMs": 1,
      "jobId": "string",
      "models": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedTimestampMs` | number |  |
| `createdTimestampMs` | number |  |
| `jobId` | string |  |
| `models` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Hume API, this operation is `GET /v0/batch/jobs/:id` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-details.md) for the provider-specific parameters and requirements.

