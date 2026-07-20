# Matterport: Get Model Access

Retrieves access details for a Matterport model.

```
GET https://connect.mindcloud.co/v1/universal/matterport/latest/actions/get-model-access
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matterport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matterport/latest/actions/get-model-access?connectionId=$CONNECTION_ID&modelId=abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matterport/latest/actions/get-model-access?${params}`, {
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
| `pageSize` | number | no | Maximum number of access records to return. Default: `25`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | no | GraphQL query for model access. Default: `query GetModelAccess($modelId: ID!, $pageSize: Int = 25, $offset: String) { model(id: $modelId) { id access(pageSize: $pageSize, offset: $offset) { nextOffset results { id } } } }`. |
| `offset` | string | no | Pagination offset returned by the previous access response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "model": {
        "access": {
          "nextOffset": "string",
          "results": [
            {}
          ]
        },
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `model` | object | Matterport model containing access records. |
| `model.access` | object | Access records page. |
| `model.access.nextOffset` | string | Offset token for the next page when present. |
| `model.access.results` | array<object> | Access records. |
| `model.id` | string | Matterport model ID. |

## Native endpoint

Through the native Matterport API, this operation is `POST api/models/graph` (base URL `https://api.matterport.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model-access.md) for the provider-specific parameters and requirements.

