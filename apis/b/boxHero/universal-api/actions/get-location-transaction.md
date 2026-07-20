# BoxHero: Get Location Transaction



```
GET https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-location-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoxHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-location-transaction?connectionId=$CONNECTION_ID&txId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "txId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-location-transaction?${params}`, {
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
| `revision` | number | no | Specific revision number of the transaction |
| `txId` | number | yes | Unique identifier for the transaction |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item": {
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
        "items": [
          {
            "deleted": true,
            "from_location_new_stock_level": 1,
            "id": 1,
            "name": "Ava Chen",
            "new_stock_level": 1,
            "quantity": 1,
            "to_location_new_stock_level": 1
          }
        ],
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item.count_of_items` | number |  |
| `item.created_at` | date |  |
| `item.created_by.deleted` | boolean |  |
| `item.created_by.id` | number |  |
| `item.created_by.name` | string |  |
| `item.from_location.deleted` | boolean |  |
| `item.from_location.id` | number |  |
| `item.from_location.name` | string |  |
| `item.id` | number |  |
| `item.items[].deleted` | boolean |  |
| `item.items[].from_location_new_stock_level` | number |  |
| `item.items[].id` | number |  |
| `item.items[].name` | string |  |
| `item.items[].new_stock_level` | number |  |
| `item.items[].quantity` | number |  |
| `item.items[].to_location_new_stock_level` | number |  |
| `item.memo` | string |  |
| `item.partner.deleted` | boolean |  |
| `item.partner.id` | number |  |
| `item.partner.name` | string |  |
| `item.revision` | number |  |
| `item.to_location.deleted` | boolean |  |
| `item.to_location.id` | number |  |
| `item.to_location.name` | string |  |
| `item.total_quantity` | number |  |
| `item.transaction_time` | date |  |
| `item.type` | string |  |
| `item.url` | string |  |

## Native endpoint

Through the native BoxHero API, this operation is `GET /v1/location-txs/:tx_id` (base URL `https://rest.boxhero-app.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location-transaction.md) for the provider-specific parameters and requirements.

