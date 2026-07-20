# Matterport: Get Model Details

Retrieves details for a Matterport model.

```
GET https://connect.mindcloud.co/v1/universal/matterport/latest/actions/get-model-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matterport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matterport/latest/actions/get-model-details?connectionId=$CONNECTION_ID&modelId=abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matterport/latest/actions/get-model-details?${params}`, {
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
| `query` | string | no | GraphQL query for model details. Default: `query GetModelDetails($modelId: ID!) { model(id: $modelId) { id name description created modified visibility accessVisibility state demo internalId } }`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "model": {
        "created": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "id": "string",
        "modified": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `model` | object | Matterport model details. |
| `model.created` | date | Creation timestamp. |
| `model.description` | string | Model description. |
| `model.id` | string | Matterport model ID. |
| `model.modified` | date | Last modified timestamp. |
| `model.name` | string | Model name. |

## Native endpoint

Through the native Matterport API, this operation is `POST api/models/graph` (base URL `https://api.matterport.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model-details.md) for the provider-specific parameters and requirements.

