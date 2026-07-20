# Open Letter Connect: List Products

Retrieves products from Open Letter Connect.

```
GET https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/list-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "backThumbnailPath": "string",
      "deliveryType": "string",
      "envelopePath": "string",
      "envelopeType": "string",
      "id": "string",
      "name": "Ava Chen",
      "paperSize": "string",
      "paperType": "string",
      "postageType": "string",
      "productSlug": "string",
      "productType": "string",
      "thumbnailPath": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backThumbnailPath` | string |  |
| `deliveryType` | string |  |
| `envelopePath` | string |  |
| `envelopeType` | string |  |
| `id` | string |  |
| `name` | string |  |
| `paperSize` | string |  |
| `paperType` | string |  |
| `postageType` | string |  |
| `productSlug` | string |  |
| `productType` | string |  |
| `thumbnailPath` | string |  |

## Native endpoint

Through the native Open Letter Connect API, this operation is `GET /products` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

