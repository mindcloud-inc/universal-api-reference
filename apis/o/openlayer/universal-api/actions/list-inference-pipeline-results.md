# Openlayer: List Inference Pipeline Results

Retrieves results for an inference pipeline in Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-inference-pipeline-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-inference-pipeline-results?connectionId=$CONNECTION_ID&inferencePipelineId=442e5769-8b85-4761-a3d5-6a7d6c080159" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inferencePipelineId": "442e5769-8b85-4761-a3d5-6a7d6c080159"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-inference-pipeline-results?${params}`, {
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
| `inferencePipelineId` | string | yes | Openlayer inference pipeline ID. Default: `442e5769-8b85-4761-a3d5-6a7d6c080159`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_meta": {},
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_meta` | object | Pagination metadata. |
| `items` | array<object> | Inference pipeline results. |

## Native endpoint

Through the native Openlayer API, this operation is `GET /inference-pipelines/:inferencePipelineId/results` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inference-pipeline-results.md) for the provider-specific parameters and requirements.

