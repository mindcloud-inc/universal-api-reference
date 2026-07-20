# Metronome: List Customer Contracts

Retrieves contracts for a customer from Metronome.

```
GET https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-customer-contracts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metronome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-customer-contracts?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-customer-contracts?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "customer_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "rate_card_id": "string",
      "starting_at": "2026-05-07T12:00:00.000Z",
      "subscriptions": [
        {
          "collection_schedule": "string",
          "fiat_credit_type_id": "string",
          "id": "string",
          "proration": {
            "invoice_behavior": "string",
            "is_prorated": true
          },
          "quantity_management_mode": "string",
          "quantity_schedule": [
            {
              "quantity": 1,
              "starting_at": "2026-05-07T12:00:00.000Z"
            }
          ],
          "starting_at": "2026-05-07T12:00:00.000Z",
          "subscription_rate": {
            "billing_frequency": "string",
            "product": {
              "id": "string",
              "name": "Ava Chen"
            }
          }
        }
      ],
      "usage_statement_schedule": {
        "billing_anchor_date": "2026-05-07T12:00:00.000Z",
        "frequency": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `created_by` | string |  |
| `customer_id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `rate_card_id` | string |  |
| `starting_at` | date |  |
| `subscriptions[].collection_schedule` | string |  |
| `subscriptions[].fiat_credit_type_id` | string |  |
| `subscriptions[].id` | string |  |
| `subscriptions[].proration.invoice_behavior` | string |  |
| `subscriptions[].proration.is_prorated` | boolean |  |
| `subscriptions[].quantity_management_mode` | string |  |
| `subscriptions[].quantity_schedule[].quantity` | number |  |
| `subscriptions[].quantity_schedule[].starting_at` | date |  |
| `subscriptions[].starting_at` | date |  |
| `subscriptions[].subscription_rate.billing_frequency` | string |  |
| `subscriptions[].subscription_rate.product.id` | string |  |
| `subscriptions[].subscription_rate.product.name` | string |  |
| `usage_statement_schedule.billing_anchor_date` | date |  |
| `usage_statement_schedule.frequency` | string |  |

## Native endpoint

Through the native Metronome API, this operation is `POST /v2/contracts/list` (base URL `https://api.metronome.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-contracts.md) for the provider-specific parameters and requirements.

