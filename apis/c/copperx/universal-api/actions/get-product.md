# Copperx: Get Product

Retrieves product record details from Copperx.

```
GET https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Copperx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-product?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-product?${params}`, {
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
| `id` | string | yes | Product ID path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "defaultPrice": {},
      "defaultPriceId": "string",
      "description": "string",
      "id": "string",
      "images": [
        {}
      ],
      "isActive": true,
      "metadata": {},
      "name": "Ava Chen",
      "unitLabel": "string",
      "updatedAt": "string",
      "url": "https://example.com",
      "visibility": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `defaultPrice` | object |  |
| `defaultPriceId` | string |  |
| `description` | string |  |
| `id` | string |  |
| `images` | array<object> |  |
| `isActive` | boolean |  |
| `metadata` | object |  |
| `name` | string |  |
| `unitLabel` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `visibility` | number |  |

## Native endpoint

Through the native Copperx API, this operation is `GET /products/{id}` (base URL `https://api.copperx.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

