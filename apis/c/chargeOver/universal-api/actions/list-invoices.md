# ChargeOver: List Invoices

Retrieves billing invoice records from ChargeOver.

```
GET https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeOver `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-invoices?${params}`, {
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
      "balance": 1,
      "customer_id": 1,
      "date": "string",
      "due_date": "string",
      "invoice_id": 1,
      "invoice_status_name": "Ava Chen",
      "is_paid": true,
      "is_void": true,
      "package_id": 1,
      "payments": 1,
      "refnumber": 1,
      "total": 1,
      "url_pdflink": "https://example.com",
      "url_self": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `customer_id` | number |  |
| `date` | string |  |
| `due_date` | string |  |
| `invoice_id` | number |  |
| `invoice_status_name` | string |  |
| `is_paid` | boolean |  |
| `is_void` | boolean |  |
| `package_id` | number |  |
| `payments` | number |  |
| `refnumber` | number |  |
| `total` | number |  |
| `url_pdflink` | string |  |
| `url_self` | string |  |

## Native endpoint

Through the native ChargeOver API, this operation is `GET /invoice` (base URL `https://{{credentials.siteName}}.chargeover.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

