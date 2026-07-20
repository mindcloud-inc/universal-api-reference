# condoo: List Account Payments

Retrieves account payments from condoo.

```
GET https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-account-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-account-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-account-payments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `frequency` | string | no | Optional payment frequency selector. |
| `processor` | string | no | Optional payment processor selector. |
| `status` | string | no | Optional payment status selector. |
| `type` | string | no | Optional payment type selector. |

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
| `currency` | string |  |
| `datetime` | date |  |
| `email` | string |  |
| `frequency` | string |  |
| `id` | number |  |
| `name` | string |  |
| `plan_id` | number |  |
| `processor` | string |  |
| `status` | boolean |  |
| `total_amount` | string |  |
| `type` | string |  |

## Native endpoint

Through the native condoo API, this operation is `GET /payments/` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-account-payments.md) for the provider-specific parameters and requirements.

