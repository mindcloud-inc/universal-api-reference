# ChargeBee: Retrieve Item Price

Retrieves an item price from ChargeBee.

```
GET https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-item-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-item-price?connectionId=$CONNECTION_ID&item_price_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "item_price_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-item-price?${params}`, {
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
| `item_price_id` | string | yes | The Chargebee item price identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency_code": "string",
      "id": "string",
      "item_id": "string",
      "name": "Ava Chen",
      "object": "string",
      "period_unit": "string",
      "price": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency_code` | string |  |
| `id` | string |  |
| `item_id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `period_unit` | string |  |
| `price` | number |  |
| `status` | string |  |

## Native endpoint

Through the native ChargeBee API, this operation is `GET item_prices/:item_price_id` (base URL `https://{{credentials.baseUrl}}.chargebee.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-item-price.md) for the provider-specific parameters and requirements.

