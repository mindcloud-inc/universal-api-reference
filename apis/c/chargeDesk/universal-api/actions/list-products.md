# ChargeDesk: List Products

Retrieves products from ChargeDesk.

```
GET https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-products?${params}`, {
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
      "amount": "string",
      "amount_formatted": "string",
      "chargeable": "string",
      "company": "string",
      "currency": "string",
      "description": "string",
      "first_seen": 1,
      "interval": "string",
      "interval_count": "string",
      "name": "Ava Chen",
      "object": "string",
      "product_id": "string",
      "quantity": "string",
      "status": "string",
      "support_url": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `amount_formatted` | string |  |
| `chargeable` | string |  |
| `company` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `first_seen` | number |  |
| `interval` | string |  |
| `interval_count` | string |  |
| `name` | string |  |
| `object` | string |  |
| `product_id` | string |  |
| `quantity` | string |  |
| `status` | string |  |
| `support_url` | string |  |
| `url` | string |  |

## Native endpoint

Through the native ChargeDesk API, this operation is `GET /products` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

