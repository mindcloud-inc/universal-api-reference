# Kladana: List Incoming Payments

Lists incoming payments in your Kladana account.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-incoming-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-incoming-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-incoming-payments?${params}`, {
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
      "agent": {},
      "applicable": true,
      "attributes": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "group": {},
      "id": "string",
      "incomingDate": "2026-05-07T12:00:00.000Z",
      "incomingNumber": "string",
      "meta": {},
      "moment": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "operations": [
        {}
      ],
      "organization": {},
      "owner": {},
      "paymentPurpose": "string",
      "sum": 1,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | object | Counterparty reference. |
| `applicable` | boolean | Whether the payment is applicable. |
| `attributes` | array<object> | Custom attributes. |
| `created` | date | Creation timestamp. |
| `group` | object | Group reference. |
| `id` | string | Payment UUID. |
| `incomingDate` | date | Incoming payment date. |
| `incomingNumber` | string | Incoming payment number. |
| `meta` | object | Kladana metadata reference. |
| `moment` | date | Payment moment. |
| `name` | string | Payment name or number. |
| `operations` | array<object> | Linked operations. |
| `organization` | object | Organization reference. |
| `owner` | object | Owner reference. |
| `paymentPurpose` | string | Payment purpose. |
| `sum` | number | Payment amount. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/paymentin` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-incoming-payments.md) for the provider-specific parameters and requirements.

