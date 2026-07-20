# Goodbarber eCommerce: Get Collection



```
GET https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-collection?connectionId=$CONNECTION_ID&collectionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-collection?${params}`, {
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
| `collectionId` | number | yes | Collection Unique ID. Default: `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "demo_products_count": 1,
      "id": 1,
      "name": "Ava Chen",
      "nb_products": 1,
      "product_positions": [
        1
      ],
      "slug": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | <div class="field_description">Timestamp of the collection creation.</div> |
| `demo_products_count` | number | <div class="field_description">Number of demo products in the collection (sample products generated automatically when GB shopping apps are created).</div> |
| `id` | number | <div class="field_description">Collection unique ID.</div> |
| `name` | string | <div class="field_description">Collection name.</div> |
| `nb_products` | number | <div class="field_description">Number of products in the collection.</div> |
| `product_positions` | array<number> | <div class="field_description">Unique IDs of the products that belong to this collection, ordered by their position in the collection.</div> |
| `slug` | string | <div class="field_description">Collection slug (used in its access URL).</div> |
| `updated_at` | string | <div class="field_description">Timestamp of the collection last update.</div> |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `GET /publicapi/v2/general/catalog/:webzine_id/collection/:collection_id/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection.md) for the provider-specific parameters and requirements.

