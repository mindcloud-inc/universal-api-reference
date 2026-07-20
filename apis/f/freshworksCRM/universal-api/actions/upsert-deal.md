# Freshworks CRM: Upsert Deal

Finds a deal in Freshworks CRM, or creates one if no match is found.

```
PUT https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/upsert-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/upsert-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deal": {},
  "uniqueIdentifier": {},
  "uniqueIdentifier.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/upsert-deal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deal": {},
    "uniqueIdentifier": {},
    "uniqueIdentifier.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deal` | object | yes |  |
| `deal.amount` | number | no |  |
| `uniqueIdentifier` | object | yes |  |
| `uniqueIdentifier.id` | string | yes |  |

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
      }
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

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/deals/upsert` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-deal.md) for the provider-specific parameters and requirements.

