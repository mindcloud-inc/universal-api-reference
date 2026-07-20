# BoxHero: List Items

Retrieves items from BoxHero.

```
GET https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoxHero `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/list-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/list-items?${params}`, {
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
| `cursor` | number | no | Cursor for the next page of items |
| `itemIds[]` | array<number> | no | Filter items by item ID |
| `limit` | number | no | Maximum number of items to return |
| `locationIds[]` | array<number> | no | Use these locations for quantity calculation |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "cursor": 1,
      "has_more": true,
      "items": [
        {
          "attrs": [
            {
              "id": 1,
              "name": "Ava Chen",
              "type": "string",
              "value": "string"
            }
          ],
          "barcode": "string",
          "cost": "string",
          "id": 1,
          "name": "Ava Chen",
          "photo_url": "https://example.com",
          "price": "string",
          "quantities": [
            {
              "location_id": 1,
              "quantity": 1
            }
          ],
          "quantity": 1,
          "sku": "string"
        }
      ],
      "limit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `cursor` | number |  |
| `has_more` | boolean |  |
| `items[].attrs[].id` | number |  |
| `items[].attrs[].name` | string |  |
| `items[].attrs[].type` | string |  |
| `items[].attrs[].value` | string |  |
| `items[].barcode` | string |  |
| `items[].cost` | string |  |
| `items[].id` | number |  |
| `items[].name` | string |  |
| `items[].photo_url` | string |  |
| `items[].price` | string |  |
| `items[].quantities[].location_id` | number |  |
| `items[].quantities[].quantity` | number |  |
| `items[].quantity` | number |  |
| `items[].sku` | string |  |
| `limit` | number |  |

## Native endpoint

Through the native BoxHero API, this operation is `GET /v1/items` (base URL `https://rest.boxhero-app.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

