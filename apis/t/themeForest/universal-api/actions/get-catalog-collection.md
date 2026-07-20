# Themeforest: Get Catalog Collection

Retrieves details for an Envato catalog collection.

```
GET https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-catalog-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Themeforest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-catalog-collection?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-catalog-collection?${params}`, {
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
| `id` | number | yes | Envato catalog collection ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Collection result page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collection": {},
      "items": [
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
| `collection` | object | Collection details. |
| `items` | array<object> | Items in the collection. |
| `pagination` | object | Pagination details. |

## Native endpoint

Through the native Themeforest API, this operation is `GET /v3/market/catalog/collection` (base URL `https://api.envato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-catalog-collection.md) for the provider-specific parameters and requirements.

