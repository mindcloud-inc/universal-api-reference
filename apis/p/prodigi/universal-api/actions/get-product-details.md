# Prodigi: Get Product Details

Retrieves details for a specific Prodigi product SKU.

```
GET https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/get-product-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prodigi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/get-product-details?connectionId=$CONNECTION_ID&sku=GLOBAL-CAN-10x10" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sku": "GLOBAL-CAN-10x10"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/get-product-details?${params}`, {
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
| `sku` | string | yes | Prodigi product SKU to retrieve. Example: `GLOBAL-CAN-10x10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "description": "string",
      "printAreas": {},
      "productDimensions": {},
      "sku": "string",
      "variants": [
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
| `attributes` | object | Available product attributes. |
| `description` | string | Product description. |
| `printAreas` | object | Available print areas. |
| `productDimensions` | object | Product dimensions. |
| `sku` | string | Product SKU. |
| `variants` | array<object> | Product variants. |

## Native endpoint

Through the native Prodigi API, this operation is `GET /products/[:sku]` (base URL `https://api.prodigi.com/v4.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-details.md) for the provider-specific parameters and requirements.

