# ChargeOver: List Customers

Retrieves customer account records from ChargeOver.

```
GET https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeOver `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-customers?${params}`, {
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
      "arr": 1,
      "balance": 1,
      "company": "string",
      "customer_id": 1,
      "customer_status_name": "Ava Chen",
      "display_as": "string",
      "mrr": 1,
      "paid": 1,
      "superuser_email": "ava@example.com",
      "superuser_name": "Ava Chen",
      "total": 1,
      "url_self": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arr` | number |  |
| `balance` | number |  |
| `company` | string |  |
| `customer_id` | number |  |
| `customer_status_name` | string |  |
| `display_as` | string |  |
| `mrr` | number |  |
| `paid` | number |  |
| `superuser_email` | string |  |
| `superuser_name` | string |  |
| `total` | number |  |
| `url_self` | string |  |

## Native endpoint

Through the native ChargeOver API, this operation is `GET /customer` (base URL `https://{{credentials.siteName}}.chargeover.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

