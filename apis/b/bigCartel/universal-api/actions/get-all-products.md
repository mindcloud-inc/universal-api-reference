# Big Cartel: Get All Products

Retrieves products from Big Cartel.

```
GET https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-all-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Big Cartel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-all-products?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-all-products?${params}`, {
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
| `accountId` | number | yes | The Big Cartel account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "defaultPrice": "string",
        "description": "string",
        "name": "Ava Chen",
        "onSale": true,
        "password": "string",
        "permalink": "https://example.com",
        "position": 1,
        "primaryImageUrl": "https://example.com",
        "status": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "url": "https://example.com"
      },
      "id": "string",
      "links": {
        "last": "https://example.com",
        "next": "https://example.com"
      },
      "meta": {
        "count": "string"
      },
      "relationships": {
        "categories": {
          "data": [
            {}
          ]
        },
        "images": {
          "data": [
            {}
          ]
        },
        "options": {
          "data": [
            {}
          ]
        },
        "shippingOptions": {
          "data": [
            {}
          ]
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.createdAt` | date |  |
| `attributes.defaultPrice` | string |  |
| `attributes.description` | string |  |
| `attributes.name` | string |  |
| `attributes.onSale` | boolean |  |
| `attributes.password` | string |  |
| `attributes.permalink` | string |  |
| `attributes.position` | number |  |
| `attributes.primaryImageUrl` | string |  |
| `attributes.status` | string |  |
| `attributes.updatedAt` | date |  |
| `attributes.url` | string |  |
| `id` | string |  |
| `links.last` | string |  |
| `links.next` | string |  |
| `meta.count` | string |  |
| `relationships.categories.data` | array<object> |  |
| `relationships.images.data` | array<object> |  |
| `relationships.options.data` | array<object> |  |
| `relationships.shippingOptions.data` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Big Cartel API, this operation is `GET /v1/accounts/[:account-id]/products` (base URL `https://api.bigcartel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-products.md) for the provider-specific parameters and requirements.

