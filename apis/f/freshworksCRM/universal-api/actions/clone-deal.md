# Freshworks CRM: Clone Deal

Creates a deal by cloning one in Freshworks CRM.

```
POST https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/clone-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/clone-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/clone-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deal": {
        "amount": "string",
        "base_currency_amount": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "deal_pipeline_id": 1,
        "deal_stage_id": 1,
        "has_products": true,
        "id": 1,
        "name": "Ava Chen",
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "users": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deal` | object |  |
| `deal.amount` | string |  |
| `deal.base_currency_amount` | string |  |
| `deal.created_at` | date |  |
| `deal.deal_pipeline_id` | number |  |
| `deal.deal_stage_id` | number |  |
| `deal.has_products` | boolean |  |
| `deal.id` | number |  |
| `deal.name` | string |  |
| `deal.updated_at` | date |  |
| `users[]` | array<object> |  |
| `users[].display_name` | string |  |
| `users[].email` | string |  |
| `users[].id` | number |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/deals/:id/clone` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clone-deal.md) for the provider-specific parameters and requirements.

