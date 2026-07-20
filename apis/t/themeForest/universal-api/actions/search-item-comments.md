# Themeforest: Search Item Comments

Finds comments for an Envato item by search term.

```
GET https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/search-item-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Themeforest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/search-item-comments?connectionId=$CONNECTION_ID&itemId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/search-item-comments?${params}`, {
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
| `itemId` | number | yes | Envato item ID whose comments should be searched. |
| `sortBy` | string | no | Comment sort order: relevance, newest, or oldest. |
| `term` | string | no | Text to search for in item comments. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Result page number. |
| `pageSize` | number | no | Number of comments per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "matches": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `matches` | array<object> | Matching comments. |
| `pagination` | object | Pagination details when returned by Envato. |

## Native endpoint

Through the native Themeforest API, this operation is `GET /v1/discovery/search/search/comment` (base URL `https://api.envato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-item-comments.md) for the provider-specific parameters and requirements.

