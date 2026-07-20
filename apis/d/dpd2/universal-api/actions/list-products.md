# Dpd2: List Products

Retrieves products from DPD, optionally filtered by storefront.

```
GET https://connect.mindcloud.co/v1/universal/dpd2/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dpd2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dpd2/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dpd2/latest/actions/list-products?${params}`, {
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
| `storefront_id` | number | no | Filter products to one storefront. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "description": "string",
      "file_name": "Ava Chen",
      "file_size": 1,
      "id": 1,
      "image_file_name": "Ava Chen",
      "image_updated_at": "string",
      "long_description": "string",
      "mime_type": "string",
      "name": "Ava Chen",
      "price": "string",
      "prices": [
        {}
      ],
      "sku": "string",
      "storefront_id": 1,
      "updated_at": "string",
      "visibility": 1,
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Product creation timestamp as returned by DPD. |
| `description` | string | Short product description. |
| `file_name` | string | Uploaded file name, if present. |
| `file_size` | number | Uploaded file size in bytes, if present. |
| `id` | number | Unique product ID. |
| `image_file_name` | string | Uploaded image file name, if present. |
| `image_updated_at` | string | Image updated timestamp, if present. |
| `long_description` | string | Long product description. |
| `mime_type` | string | Uploaded file MIME type, if present. |
| `name` | string | Product name. |
| `price` | string | Default product price. |
| `prices` | array<object> | Per-price option records. |
| `sku` | string | Product SKU. |
| `storefront_id` | number | Owning storefront ID. |
| `updated_at` | string | Product update timestamp as returned by DPD, or null. |
| `visibility` | number | Visibility flag where 1 means displayed. |
| `weight` | number | Product weight, if present. |

## Native endpoint

Through the native Dpd2 API, this operation is `GET /products` (base URL `https://api.getdpd.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

