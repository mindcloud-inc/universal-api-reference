# Keysender: Get Product By SKU

Retrieves a product from Keysender by SKU.

```
GET https://connect.mindcloud.co/v1/universal/keysender/latest/actions/get-product-by-sku
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keysender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/get-product-by-sku?connectionId=$CONNECTION_ID&sku=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sku": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keysender/latest/actions/get-product-by-sku?${params}`, {
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
| `sku` | string | yes | The product SKU. |
| `additionalInformation` | boolean | no | Include expanded product information when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "description": "string",
      "developer": "string",
      "id": "string",
      "name": "Ava Chen",
      "publisher": "string",
      "purchasePrice": 1,
      "qty": 1,
      "regularPrice": 1,
      "releaseDate": "string",
      "sku": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string | Product currency. |
| `description` | string | Product description. |
| `developer` | string | Product developer. |
| `id` | string | Product identifier. |
| `name` | string | Product name. |
| `publisher` | string | Product publisher. |
| `purchasePrice` | number | Purchase price. |
| `qty` | number | Available stock quantity. |
| `regularPrice` | number | Regular catalog price. |
| `releaseDate` | string | Release date text from the provider. |
| `sku` | string | Product SKU. |
| `type` | string | Product type. |
| `updatedAt` | date | UTC timestamp for the last product update. |

## Native endpoint

Through the native Keysender API, this operation is `GET /catalog/products/:sku` (base URL `https://panel.keysender.co.uk/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-by-sku.md) for the provider-specific parameters and requirements.

