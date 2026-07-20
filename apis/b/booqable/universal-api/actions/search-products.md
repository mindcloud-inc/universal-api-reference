# Booqable: Search Products

Finds products in Booqable by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/booqable/latest/actions/search-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Booqable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/search-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/booqable/latest/actions/search-products?${params}`, {
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
| `filter` | object | no | Hash of product filters using documented field/operator keys. |
| `include` | string | no | Comma-separated relationships to sideload, for example barcode,inventory_levels,photo. Example: `barcode,inventory_levels,photo`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "archived": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "productType": "string",
        "slug": "string",
        "trackingType": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.archived` | boolean | Whether the product is archived. |
| `attributes.createdAt` | date | When the product was created. |
| `attributes.name` | string | Product name. |
| `attributes.productType` | string | Product type. |
| `attributes.slug` | string | Store slug. |
| `attributes.trackingType` | string | Tracking type. |
| `attributes.updatedAt` | date | When the product was last updated. |
| `id` | string | Product ID. |
| `relationships` | object | Product relationships. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Booqable API, this operation is `POST /products/search` (base URL `https://mindcloud.booqable.com/api/4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-products.md) for the provider-specific parameters and requirements.

