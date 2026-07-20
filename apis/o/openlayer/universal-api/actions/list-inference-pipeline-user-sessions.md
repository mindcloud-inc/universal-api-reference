# Openlayer: List Inference Pipeline User Sessions



```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-inference-pipeline-user-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-inference-pipeline-user-sessions?connectionId=$CONNECTION_ID&inferencePipelineId=442e5769-8b85-4761-a3d5-6a7d6c080159&userId=mindcloud-user-1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inferencePipelineId": "442e5769-8b85-4761-a3d5-6a7d6c080159",
  "userId": "mindcloud-user-1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-inference-pipeline-user-sessions?${params}`, {
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
| `inferencePipelineId` | string | yes | The inference pipeline ID. Default: `442e5769-8b85-4761-a3d5-6a7d6c080159`. |
| `userId` | string | yes | The user ID to list sessions for. Default: `mindcloud-user-1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_meta": {
        "page": 1,
        "perPage": 1,
        "totalItems": 1,
        "totalPages": 1
      },
      "items": [
        {
          "cost": 1,
          "dateCreated": "string",
          "dateOfFirstRecord": "string",
          "dateOfLastRecord": "string",
          "duration": 1,
          "id": "string",
          "latency": 1,
          "records": 1,
          "tokens": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_meta.page` | number |  |
| `_meta.perPage` | number |  |
| `_meta.totalItems` | number |  |
| `_meta.totalPages` | number |  |
| `items[].cost` | number |  |
| `items[].dateCreated` | string |  |
| `items[].dateOfFirstRecord` | string |  |
| `items[].dateOfLastRecord` | string |  |
| `items[].duration` | number |  |
| `items[].id` | string |  |
| `items[].latency` | number |  |
| `items[].records` | number |  |
| `items[].tokens` | number |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /inference-pipelines/:inferencePipelineId/user/sessions` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inference-pipeline-user-sessions.md) for the provider-specific parameters and requirements.

