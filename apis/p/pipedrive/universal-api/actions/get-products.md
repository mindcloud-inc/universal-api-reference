# Pipedrive: Get Products

Retrieves products from Pipedrive.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-products?${params}`, {
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
| `limit` | number | no | Max number of products to return. |
| `cursor` | string | no | Pagination cursor from previous response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addTime": "string",
      "category": {},
      "code": "string",
      "description": "string",
      "id": 1,
      "isDeleted": true,
      "isLinkable": true,
      "name": "Ava Chen",
      "ownerId": 1,
      "prices": [
        {
          "cost": 1,
          "currency": "string",
          "directCost": 1,
          "notes": "string",
          "price": 1,
          "productId": 1
        }
      ],
      "tax": 1,
      "unit": "string",
      "updateTime": "string",
      "visibleTo": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addTime` | string |  |
| `category` | object |  |
| `code` | string |  |
| `description` | string |  |
| `id` | number |  |
| `isDeleted` | boolean |  |
| `isLinkable` | boolean |  |
| `name` | string |  |
| `ownerId` | number |  |
| `prices[].cost` | number |  |
| `prices[].currency` | string |  |
| `prices[].directCost` | number |  |
| `prices[].notes` | string |  |
| `prices[].price` | number |  |
| `prices[].productId` | number |  |
| `tax` | number |  |
| `unit` | string |  |
| `updateTime` | string |  |
| `visibleTo` | number |  |

## Native endpoint

Through the native Pipedrive API, this operation is `GET v2/products` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-products.md) for the provider-specific parameters and requirements.

