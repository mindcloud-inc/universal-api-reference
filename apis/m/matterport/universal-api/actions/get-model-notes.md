# Matterport: Get Model Notes

Retrieves notes from a Matterport model.

```
GET https://connect.mindcloud.co/v1/universal/matterport/latest/actions/get-model-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matterport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matterport/latest/actions/get-model-notes?connectionId=$CONNECTION_ID&modelId=abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matterport/latest/actions/get-model-notes?${params}`, {
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
| `query` | string | no | GraphQL query for model notes. Default: `query GetModelNotes($modelId: ID!) { model(id: $modelId) { id notes { id label enabled anchorPosition { x y z } } } }`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "model": {
        "id": "string",
        "notes": [
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
| `model` | object | Matterport model containing notes. |
| `model.id` | string | Matterport model ID. |
| `model.notes` | array<object> | Notes in the model. |

## Native endpoint

Through the native Matterport API, this operation is `POST api/models/graph` (base URL `https://api.matterport.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model-notes.md) for the provider-specific parameters and requirements.

