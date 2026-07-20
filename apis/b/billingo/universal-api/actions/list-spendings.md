# Billingo: List Spendings

Retrieves spending items from Billingo by due date.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/list-spendings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/list-spendings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/list-spendings?${params}`, {
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
      "category": "string",
      "currency": "string",
      "due_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "invoice_date": "2026-05-07T12:00:00.000Z",
      "invoice_number": "string",
      "organization_id": 1,
      "partner": {},
      "payment_method": "string",
      "total_gross": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `currency` | string |  |
| `due_date` | date |  |
| `id` | number |  |
| `invoice_date` | date |  |
| `invoice_number` | string |  |
| `organization_id` | number |  |
| `partner` | object |  |
| `payment_method` | string |  |
| `total_gross` | number |  |

## Native endpoint

Through the native Billingo API, this operation is `GET /spendings` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-spendings.md) for the provider-specific parameters and requirements.

