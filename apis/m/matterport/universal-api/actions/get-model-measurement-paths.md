# Matterport: Get Model Measurement Paths

Retrieves measurement paths from a Matterport model.

```
GET https://connect.mindcloud.co/v1/universal/matterport/latest/actions/get-model-measurement-paths
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matterport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matterport/latest/actions/get-model-measurement-paths?connectionId=$CONNECTION_ID&modelId=abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matterport/latest/actions/get-model-measurement-paths?${params}`, {
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
| `modelId` | string | yes | Matterport model ID. Example: `abc123`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | no | GraphQL query for measurement paths. Default: `query GetModelMeasurementPaths($modelId: ID!) { model(id: $modelId) { id measurementPaths { id label enabled } } }`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "model": {
        "id": "string",
        "measurementPaths": [
          {}
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `model` | object | Matterport model containing measurement paths. |
| `model.id` | string | Matterport model ID. |
| `model.measurementPaths` | array<object> | Measurement paths in the model. |

## Native endpoint

Through the native Matterport API, this operation is `POST api/models/graph` (base URL `https://api.matterport.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model-measurement-paths.md) for the provider-specific parameters and requirements.

