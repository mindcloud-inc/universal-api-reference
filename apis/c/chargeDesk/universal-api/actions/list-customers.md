# ChargeDesk: List Customers

Retrieves customers from ChargeDesk.

```
GET https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-customers?${params}`, {
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
      "card_on_file": "string",
      "charges": 1,
      "company": "string",
      "country": "string",
      "customer_id": "string",
      "description": "string",
      "email": "ava@example.com",
      "first_seen": 1,
      "gateway_url": "https://example.com",
      "manage_url": "https://example.com",
      "methods_active": [
        "string"
      ],
      "methods_supported": [
        "string"
      ],
      "name": "Ava Chen",
      "object": "string",
      "phone": "string",
      "username": "Ava Chen",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `card_on_file` | string |  |
| `charges` | number |  |
| `company` | string |  |
| `country` | string |  |
| `customer_id` | string |  |
| `description` | string |  |
| `email` | string |  |
| `first_seen` | number |  |
| `gateway_url` | string |  |
| `manage_url` | string |  |
| `methods_active` | array<string> |  |
| `methods_supported` | array<string> |  |
| `name` | string |  |
| `object` | string |  |
| `phone` | string |  |
| `username` | string |  |
| `website` | string |  |

## Native endpoint

Through the native ChargeDesk API, this operation is `GET /customers` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

