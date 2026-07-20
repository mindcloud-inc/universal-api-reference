# Hiboutik: Get Product Barcode

Retrieves a product barcode from Hiboutik.

```
GET https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/get-product-barcode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hiboutik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/get-product-barcode?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/get-product-barcode?${params}`, {
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
| `productId` | string | no | The Hiboutik product id. |
| `sizeId` | string | no | The Hiboutik product size id. |
| `storeId` | string | no | The Hiboutik store id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "barcode": "string",
      "stockAvailable": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `barcode` | string |  |
| `stockAvailable` | string |  |

## Native endpoint

Through the native Hiboutik API, this operation is `GET /products_barcode/:store_id/:product_id/:size_id/` (base URL `https://mindcloudhiboutik20260402.hiboutik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-barcode.md) for the provider-specific parameters and requirements.

