# Matterport: List Models

Retrieves models from your Matterport account.

```
GET https://connect.mindcloud.co/v1/universal/matterport/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matterport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matterport/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matterport/latest/actions/list-models?${params}`, {
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
| `modelQuery` | string | no | Matterport model search query. Use * for all active models. Default: `*`. Example: `*`. |
| `pageSize` | number | no | Maximum number of models to return. Default: `10`. Example: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | no | Hidden GraphQL query for listing models. Default: `query ListModels($modelQuery: String = \"*\", $pageSize: Int = 10, $offset: String) { models(query: $modelQuery, pageSize: $pageSize, offset: $offset) { totalResults nextOffset results { id name created modified visibility accessVisibility state demo internalId } } }`. |
| `offset` | string | no | Next page offset returned by a previous models query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "models": {
        "nextOffset": "string",
        "results": [
          {}
        ],
        "totalResults": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `models` | object | Matterport model search results. |
| `models.nextOffset` | string | Offset token for the next page when present. |
| `models.results` | array<object> | Matching Matterport models. |
| `models.totalResults` | number | Total number of matching models. |

## Native endpoint

Through the native Matterport API, this operation is `POST api/models/graph` (base URL `https://api.matterport.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

