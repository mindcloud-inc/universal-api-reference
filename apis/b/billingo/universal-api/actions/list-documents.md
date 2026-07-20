# Billingo: List Documents

Retrieves document records from your Billingo account.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/list-documents?${params}`, {
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
      "cancelled": true,
      "currency": "string",
      "gross_total": 1,
      "id": 1,
      "invoice_date": "2026-05-07T12:00:00.000Z",
      "invoice_number": "string",
      "items": [
        {}
      ],
      "partner": {},
      "payment_method": "string",
      "payment_status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelled` | boolean |  |
| `currency` | string |  |
| `gross_total` | number |  |
| `id` | number |  |
| `invoice_date` | date |  |
| `invoice_number` | string |  |
| `items` | array<object> |  |
| `partner` | object |  |
| `payment_method` | string |  |
| `payment_status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Billingo API, this operation is `GET /documents` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

