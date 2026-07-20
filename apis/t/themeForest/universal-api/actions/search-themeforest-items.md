# Themeforest: Search ThemeForest Items

Finds ThemeForest items by search term.

```
GET https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/search-themeforest-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Themeforest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/search-themeforest-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/search-themeforest-items?${params}`, {
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
| `category` | string | no | ThemeForest category filter. |
| `sortBy` | string | no | Sort field supported by Envato discovery search. |
| `sortDirection` | string | no | Sort direction supported by Envato discovery search. |
| `term` | string | no | Search text for matching ThemeForest items. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Result page number. |
| `pageSize` | number | no | Number of results per page. |

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
| `matches` | array<object> | Matching Envato discovery items. |
| `pagination` | object | Pagination details when returned by Envato. |

## Native endpoint

Through the native Themeforest API, this operation is `GET /v1/discovery/search/search/item` (base URL `https://api.envato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-themeforest-items.md) for the provider-specific parameters and requirements.

