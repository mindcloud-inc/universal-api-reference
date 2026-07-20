# Natif.ai: List Reseller Customers

Retrieves reseller customer records from Natif.ai.

```
GET https://connect.mindcloud.co/v1/universal/natifai/latest/actions/list-reseller-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Natif.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/list-reseller-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/natifai/latest/actions/list-reseller-customers?${params}`, {
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
      "customer_id": "string",
      "name": "Ava Chen",
      "organizational_info": {},
      "use_technical_interface": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer_id` | string |  |
| `name` | string |  |
| `organizational_info` | object |  |
| `use_technical_interface` | boolean |  |

## Native endpoint

Through the native Natif.ai API, this operation is `GET /reseller/customers` (base URL `https://api.natif.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reseller-customers.md) for the provider-specific parameters and requirements.

