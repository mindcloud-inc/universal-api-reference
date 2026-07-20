# Freshworks CRM: Create Deal

Creates a new deal in Freshworks CRM.

```
POST https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deal` | object | no | Deal payload object as documented by Freshworks CRM. |
| `deal.amount` | number | no |  |
| `deal.contactsAddedList[]` | array<number> | no |  |
| `deal.customField` | object | no |  |
| `deal.customField.cfNumberOfAgents` | number | no |  |
| `deal.name` | string | no |  |
| `deal.salesAccount` | object | no |  |
| `deal.salesAccount.name` | string | no |  |
| `deal.salesAccountId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deal": {
        "age": 1,
        "amount": "string",
        "base_currency_amount": "string",
        "closed_date": "2026-05-07T12:00:00.000Z",
        "created_at": "2026-05-07T12:00:00.000Z",
        "creater_id": 1,
        "custom_field": {
          "cf_number_of_agents": 1
        },
        "expected_close": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "name": "Ava Chen",
        "probability": 1,
        "stage_updated_time": "2026-05-07T12:00:00.000Z",
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "users": [
        {
          "display_name": "Ava Chen",
          "email": "ava@example.com",
          "id": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deal.age` | number | Deal age. |
| `deal.amount` | string | Deal amount. |
| `deal.base_currency_amount` | string | Amount in base currency. |
| `deal.closed_date` | date | Closed date. |
| `deal.created_at` | date | Created timestamp. |
| `deal.creater_id` | number | Creator user id. |
| `deal.custom_field.cf_number_of_agents` | number | Custom number-of-agents field. |
| `deal.expected_close` | date | Expected close date. |
| `deal.id` | number | Deal identifier. |
| `deal.name` | string | Deal name. |
| `deal.probability` | number | Deal probability. |
| `deal.stage_updated_time` | date | Stage updated timestamp. |
| `deal.updated_at` | date | Updated timestamp. |
| `users[].display_name` | string | Related user display name. |
| `users[].email` | string | Related user email. |
| `users[].id` | number | Related user id. |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST api/deals` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

