# Themeforest: List Author Sales

Retrieves author sales from Envato Market.

```
GET https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/list-author-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Themeforest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/list-author-sales?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/list-author-sales?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Author sales result page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sales": [
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
| `sales` | array<object> | Author sales. |

## Native endpoint

Through the native Themeforest API, this operation is `GET /v3/market/author/sales` (base URL `https://api.envato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-author-sales.md) for the provider-specific parameters and requirements.

