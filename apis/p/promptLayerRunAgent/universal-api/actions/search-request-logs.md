# PromptLayer Run Agent: Search Request Logs

Finds request logs in PromptLayer.

```
GET https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/search-request-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/search-request-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/search-request-logs?${params}`, {
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
| `q` | string | no | Free-text search query for request logs. Example: `MindCloud stage3 request log alpha`. |
| `includePromptName` | boolean | no | Whether to include prompt names in each search result. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterGroup` | object | no | Structured filter group with nested AND or OR logic. |
| `page` | number | no | Page number for pagination. Default: `1`. |
| `perPage` | number | no | Number of results per page. Default: `10`. |
| `sortBy` | list | no | Field to sort request logs by. |
| `sortOrder` | list | no | Sort direction to use with sortBy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasNext": true,
      "hasPrev": true,
      "items": [
        {}
      ],
      "nextNum": 1,
      "page": 1,
      "pages": 1,
      "perPage": 1,
      "prevNum": 1,
      "success": true,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasNext` | boolean |  |
| `hasPrev` | boolean |  |
| `items` | array<object> |  |
| `nextNum` | number |  |
| `page` | number |  |
| `pages` | number |  |
| `perPage` | number |  |
| `prevNum` | number |  |
| `success` | boolean |  |
| `total` | number |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `POST /api/public/v2/requests/search` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-request-logs.md) for the provider-specific parameters and requirements.

