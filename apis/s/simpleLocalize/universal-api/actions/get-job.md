# SimpleLocalize: Get Job

Retrieves a job from SimpleLocalize.

```
GET https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-job?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "jobId": "string",
      "message": "string",
      "metadata": {},
      "progress": 1,
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `jobId` | string |  |
| `message` | string |  |
| `metadata` | object |  |
| `progress` | number |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SimpleLocalize API, this operation is `GET /api/v2/jobs/{jobId}` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

