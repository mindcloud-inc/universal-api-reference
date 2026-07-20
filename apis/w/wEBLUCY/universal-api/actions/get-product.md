# WEBLUCY: Get Product

Retrieves a product from WEBLUCY.

```
GET https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/get-product?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/get-product?${params}`, {
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
| `id` | string | yes | The product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {}
      ],
      "description": "string",
      "hidden": true,
      "id": 1,
      "images": [
        {}
      ],
      "options": [
        {}
      ],
      "seoDescription": "string",
      "subscription": {},
      "title": "string",
      "type": "string",
      "url": "https://example.com",
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
| `categories` | array<object> |  |
| `description` | string |  |
| `hidden` | boolean |  |
| `id` | number |  |
| `images` | array<object> |  |
| `options` | array<object> |  |
| `seoDescription` | string |  |
| `subscription` | object |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |
| `variants` | array<object> |  |

## Native endpoint

Through the native WEBLUCY API, this operation is `GET /products/{id}` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

