# Booqable: Create Product

Creates a new product in Booqable.

```
POST https://connect.mindcloud.co/v1/universal/booqable/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Booqable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/booqable/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Product payload. Enter the inner JSON:API resource object, for example type plus attributes. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
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

Through the native Booqable API, this operation is `POST /products` (base URL `https://mindcloud.booqable.com/api/4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

