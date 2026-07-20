# Hiboutik: Search Products By Barcode

Finds products in Hiboutik by barcode.

```
GET https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/search-products-by-barcode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hiboutik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/search-products-by-barcode?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/search-products-by-barcode?${params}`, {
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
| `query` | string | no | The product barcode search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "productId": 1,
      "productModel": "string",
      "productSize": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `productId` | number |  |
| `productModel` | string |  |
| `productSize` | number |  |

## Native endpoint

Through the native Hiboutik API, this operation is `GET /products/search/barcode/:q/` (base URL `https://mindcloudhiboutik20260402.hiboutik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-products-by-barcode.md) for the provider-specific parameters and requirements.

