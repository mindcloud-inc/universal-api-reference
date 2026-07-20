# DevCycle: Get Metric

Retrieves a metric from DevCycle.

```
GET https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-metric
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DevCycle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-metric?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-metric?${params}`, {
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
| `key` | string | no | Metric key. Default: `mindcloud-signups`. |
| `project` | string | no | Project key. Default: `mindcloud`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "dimension": "string",
      "event": "string",
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "optimize": "string",
      "projectId": "string",
      "source": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `dimension` | string |  |
| `event` | string |  |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `optimize` | string |  |
| `projectId` | string |  |
| `source` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native DevCycle API, this operation is `GET /v1/projects/:project/metrics/:key` (base URL `https://api.devcycle.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-metric.md) for the provider-specific parameters and requirements.

