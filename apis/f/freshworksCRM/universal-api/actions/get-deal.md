# Freshworks CRM: Get Deal

Retrieves a deal from Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-deal?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-deal?${params}`, {
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
| `dealId` | number | no | Unique deal identifier. |

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
        "custom_field": {
          "cf_number_of_agents": 1
        },
        "expected_close": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "name": "Ava Chen",
        "owner_id": 1,
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
| `deal.custom_field.cf_number_of_agents` | number | Custom number-of-agents field. |
| `deal.expected_close` | date | Expected close date. |
| `deal.id` | number | Deal identifier. |
| `deal.name` | string | Deal name. |
| `deal.owner_id` | number | Deal owner user id. |
| `deal.probability` | number | Deal probability. |
| `deal.stage_updated_time` | date | Stage updated timestamp. |
| `deal.updated_at` | date | Updated timestamp. |
| `users[].display_name` | string | Related user display name. |
| `users[].email` | string | Related user email. |
| `users[].id` | number | Related user id. |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET api/deals/:id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal.md) for the provider-specific parameters and requirements.

