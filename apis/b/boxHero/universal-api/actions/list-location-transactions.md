# BoxHero: List Location Transactions



```
GET https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/list-location-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoxHero `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/list-location-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/list-location-transactions?${params}`, {
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
| `cursor` | number | no | Cursor for the next page of transactions |
| `limit` | number | no | Maximum number of transactions to return |
| `type` | string | no | Filter transactions by type |

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
          "count_of_items": 1,
          "created_at": "2026-05-07T12:00:00.000Z",
          "created_by": {
            "deleted": true,
            "id": 1,
            "name": "Ava Chen"
          },
          "from_location": {
            "deleted": true,
            "id": 1,
            "name": "Ava Chen"
          },
          "id": 1,
          "memo": "string",
          "partner": {
            "deleted": true,
            "id": 1,
            "name": "Ava Chen"
          },
          "revision": 1,
          "to_location": {
            "deleted": true,
            "id": 1,
            "name": "Ava Chen"
          },
          "total_quantity": 1,
          "transaction_time": "2026-05-07T12:00:00.000Z",
          "type": "string",
          "url": "https://example.com"
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
| `items[].count_of_items` | number |  |
| `items[].created_at` | date |  |
| `items[].created_by.deleted` | boolean |  |
| `items[].created_by.id` | number |  |
| `items[].created_by.name` | string |  |
| `items[].from_location.deleted` | boolean |  |
| `items[].from_location.id` | number |  |
| `items[].from_location.name` | string |  |
| `items[].id` | number |  |
| `items[].memo` | string |  |
| `items[].partner.deleted` | boolean |  |
| `items[].partner.id` | number |  |
| `items[].partner.name` | string |  |
| `items[].revision` | number |  |
| `items[].to_location.deleted` | boolean |  |
| `items[].to_location.id` | number |  |
| `items[].to_location.name` | string |  |
| `items[].total_quantity` | number |  |
| `items[].transaction_time` | date |  |
| `items[].type` | string |  |
| `items[].url` | string |  |
| `limit` | number |  |

## Native endpoint

Through the native BoxHero API, this operation is `GET /v1/location-txs` (base URL `https://rest.boxhero-app.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-location-transactions.md) for the provider-specific parameters and requirements.

