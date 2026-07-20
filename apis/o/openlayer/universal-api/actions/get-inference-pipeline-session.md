# Openlayer: Get Inference Pipeline Session

Retrieves a session for an inference pipeline in Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-inference-pipeline-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-inference-pipeline-session?connectionId=$CONNECTION_ID&inferencePipelineId=442e5769-8b85-4761-a3d5-6a7d6c080159&sessionId=mindcloud-session-1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inferencePipelineId": "442e5769-8b85-4761-a3d5-6a7d6c080159",
  "sessionId": "mindcloud-session-1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-inference-pipeline-session?${params}`, {
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
| `sessionId` | string | yes | The session ID to aggregate. Default: `mindcloud-session-1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": 1,
      "dateCreated": "string",
      "dateOfFirstRecord": "string",
      "dateOfLastRecord": "string",
      "duration": 1,
      "id": "string",
      "latency": 1,
      "records": 1,
      "tokens": 1,
      "userIds": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | number |  |
| `dateCreated` | string |  |
| `dateOfFirstRecord` | string |  |
| `dateOfLastRecord` | string |  |
| `duration` | number |  |
| `id` | string |  |
| `latency` | number |  |
| `records` | number |  |
| `tokens` | number |  |
| `userIds[]` | array<string> |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /inference-pipelines/:inferencePipelineId/session` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inference-pipeline-session.md) for the provider-specific parameters and requirements.

