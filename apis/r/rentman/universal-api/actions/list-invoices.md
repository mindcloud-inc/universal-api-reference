# Rentman: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-invoices?${params}`, {
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
      "account_manager": "string",
      "contact": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "customer": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "date_sent": "2026-05-07T12:00:00.000Z",
      "days_after_expiry": 1,
      "displayname": "Ava Chen",
      "expiration": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "final_payment_reminder_sent": "2026-05-07T12:00:00.000Z",
      "finalized": true,
      "from_project": true,
      "id": 1,
      "integration_reference_id": "string",
      "invoicetype": "string",
      "is_paid": true,
      "modified": "2026-05-07T12:00:00.000Z",
      "number": "string",
      "outstanding_balance": 1,
      "payment_date": "2026-05-07T12:00:00.000Z",
      "payment_reminder_sent": 1,
      "price": 1,
      "price_invat": 1,
      "procent": 1,
      "project": "string",
      "subject": "string",
      "sum_factuurregels": 1,
      "tags": "string",
      "total_paid": 1,
      "updateHash": "string",
      "vat_amount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_manager` | string |  |
| `contact` | string |  |
| `created` | date |  |
| `creator` | string |  |
| `customer` | string |  |
| `date` | date |  |
| `date_sent` | date |  |
| `days_after_expiry` | number |  |
| `displayname` | string |  |
| `expiration` | date |  |
| `filename` | string |  |
| `final_payment_reminder_sent` | date |  |
| `finalized` | boolean |  |
| `from_project` | boolean |  |
| `id` | number |  |
| `integration_reference_id` | string |  |
| `invoicetype` | string |  |
| `is_paid` | boolean |  |
| `modified` | date |  |
| `number` | string |  |
| `outstanding_balance` | number |  |
| `payment_date` | date |  |
| `payment_reminder_sent` | number |  |
| `price` | number |  |
| `price_invat` | number |  |
| `procent` | number |  |
| `project` | string |  |
| `subject` | string |  |
| `sum_factuurregels` | number |  |
| `tags` | string |  |
| `total_paid` | number |  |
| `updateHash` | string |  |
| `vat_amount` | number |  |

## Native endpoint

Through the native Rentman API, this operation is `GET /invoices` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

