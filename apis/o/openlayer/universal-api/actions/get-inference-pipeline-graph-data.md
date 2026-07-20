# Openlayer: Get Inference Pipeline Graph Data

Retrieves graph data for an inference pipeline in Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-inference-pipeline-graph-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-inference-pipeline-graph-data?connectionId=$CONNECTION_ID&inferencePipelineId=442e5769-8b85-4761-a3d5-6a7d6c080159" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inferencePipelineId": "442e5769-8b85-4761-a3d5-6a7d6c080159"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-inference-pipeline-graph-data?${params}`, {
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
      "dataVolumeGraphs": {},
      "dateLastSampleReceived": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataVolumeGraphs` | object | Volume graphs grouped by time period. |
| `dateLastSampleReceived` | date | Timestamp of the last received sample. |

## Native endpoint

Through the native Openlayer API, this operation is `GET /inference-pipelines/:inferencePipelineId/graph-data` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inference-pipeline-graph-data.md) for the provider-specific parameters and requirements.

