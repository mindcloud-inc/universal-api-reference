# Geral: List Payments

Retrieves account payments from Geral.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-payments?${params}`, {
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
      "currency": "string",
      "datetime": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "frequency": "string",
      "id": 1,
      "name": "Ava Chen",
      "plan_id": 1,
      "processor": "string",
      "status": true,
      "total_amount": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string | Payment currency. |
| `datetime` | date | Creation timestamp. |
| `email` | string | Billing email. |
| `frequency` | string | Billing frequency. |
| `id` | number | Payment ID. |
| `name` | string | Billing name. |
| `plan_id` | number | Plan ID. |
| `processor` | string | Payment processor. |
| `status` | boolean | Payment status. |
| `total_amount` | string | Total payment amount. |
| `type` | string | Payment type. |

## Native endpoint

Through the native Geral API, this operation is `GET /payments/` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

