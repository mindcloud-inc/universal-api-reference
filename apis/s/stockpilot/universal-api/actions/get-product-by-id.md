# Stockpilot: Get Product by ID

Retrieves a product from Stockpilot.

```
GET https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-product-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-product-by-id?connectionId=$CONNECTION_ID&id=660724" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "660724"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-product-by-id?${params}`, {
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
| `id` | number | yes | Internal product ID Example: `660724`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand": 1,
      "category": 1,
      "description": "string",
      "image_url": "https://example.com",
      "is_active": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | number | Brand ID |
| `category` | number | Category ID |
| `description` | string | Product description |
| `image_url` | string | Product image URL |
| `is_active` | boolean | Whether the product is active |
| `title` | string | Product title |

## Native endpoint

Through the native Stockpilot API, this operation is `GET /products/get` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-by-id.md) for the provider-specific parameters and requirements.

