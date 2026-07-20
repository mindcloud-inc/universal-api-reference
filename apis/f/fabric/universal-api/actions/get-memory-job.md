# Fabric: Get Memory Job

Retrieves a memory job from Fabric.

```
GET https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-memory-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fabric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-memory-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-memory-job?${params}`, {
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
| `jobId` | string | yes | The Fabric memory job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "modifiedAt": "string",
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
| `createdAt` | string |  |
| `id` | string |  |
| `modifiedAt` | string |  |
| `result` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Fabric API, this operation is `GET /v2/memories/jobs/{jobId}` (base URL `https://api.fabric.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-memory-job.md) for the provider-specific parameters and requirements.

