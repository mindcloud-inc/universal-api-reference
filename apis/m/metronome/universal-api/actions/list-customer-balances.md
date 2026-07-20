# Metronome: List Customer Balances

Retrieves balances for a customer from Metronome.

```
GET https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-customer-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metronome `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-customer-balances?connectionId=$CONNECTION_ID&limit=25&offset=0&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-customer-balances?${params}`, {
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
| `customerId` | string | yes | The customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_schedule": {
        "credit_type": {
          "id": "string",
          "name": "Ava Chen"
        },
        "schedule_items": [
          {
            "amount": 1,
            "ending_before": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "starting_at": "2026-05-07T12:00:00.000Z"
          }
        ]
      },
      "amount": 1,
      "balance": 1,
      "contract": {
        "id": "string"
      },
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "priority": 1,
      "product": {
        "id": "string",
        "name": "Ava Chen"
      },
      "rate_type": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_schedule.credit_type.id` | string |  |
| `access_schedule.credit_type.name` | string |  |
| `access_schedule.schedule_items[].amount` | number |  |
| `access_schedule.schedule_items[].ending_before` | date |  |
| `access_schedule.schedule_items[].id` | string |  |
| `access_schedule.schedule_items[].starting_at` | date |  |
| `amount` | number |  |
| `balance` | number |  |
| `contract.id` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `priority` | number |  |
| `product.id` | string |  |
| `product.name` | string |  |
| `rate_type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Metronome API, this operation is `POST /v1/contracts/customerBalances/list` (base URL `https://api.metronome.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customer-balances.md) for the provider-specific parameters and requirements.

