# Themeforest: Get Catalog Item

Retrieves details for an Envato catalog item.

```
GET https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-catalog-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Themeforest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-catalog-item?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-catalog-item?${params}`, {
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
| `id` | number | yes | Envato catalog item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author_username": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "number_of_sales": 1,
      "site": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author_username` | string | Author username. |
| `id` | number | Envato item ID. |
| `name` | string | Item name. |
| `number_of_sales` | number | Item sales count. |
| `site` | string | Envato site. |
| `url` | string | Item URL. |

## Native endpoint

Through the native Themeforest API, this operation is `GET /v3/market/catalog/item` (base URL `https://api.envato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-catalog-item.md) for the provider-specific parameters and requirements.

