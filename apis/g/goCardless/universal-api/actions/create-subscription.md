# GoCardless: Create Subscription

Creates a new subscription in GoCardless.

```
POST https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptions.amount": 1,
  "subscriptions.currency": "string",
  "subscriptions.interval_unit": "string",
  "subscriptions.links.mandate": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptions.amount": 1,
    "subscriptions.currency": "string",
    "subscriptions.interval_unit": "string",
    "subscriptions.links.mandate": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptions.amount` | number | yes |  |
| `subscriptions.currency` | string | yes |  |
| `subscriptions.interval_unit` | string | yes |  |
| `subscriptions.links.mandate` | string | yes |  |
| `subscriptions.interval` | number | no |  |
| `subscriptions.day_of_month` | number | no |  |
| `subscriptions.month` | string | no |  |
| `subscriptions.start_date` | date | no |  |
| `subscriptions.count` | number | no |  |
| `subscriptions.end_date` | date | no |  |
| `subscriptions.name` | string | no |  |
| `subscriptions.app_fee` | number | no |  |
| `subscriptions.metadata` | object | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptions.payment_reference` | string | no |  |
| `subscriptions.retry_if_possible` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscriptions": {
        "amount": 1,
        "appFee": 1,
        "count": {},
        "createdAt": "string",
        "currency": "string",
        "dayOfMonth": 1,
        "earliestChargeDateAfterResume": {},
        "endDate": {},
        "id": "string",
        "interval": 1,
        "intervalUnit": "string",
        "links": {
          "mandate": "https://example.com"
        },
        "metadata": {
          "source": "string"
        },
        "month": {},
        "name": "Ava Chen",
        "parentPlanPaused": true,
        "paymentReference": {},
        "retryIfPossible": true,
        "startDate": "string",
        "status": "string",
        "upcomingPayments": [
          {
            "amount": 1,
            "chargeDate": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscriptions.amount` | number |  |
| `subscriptions.appFee` | number |  |
| `subscriptions.count` | object |  |
| `subscriptions.createdAt` | string |  |
| `subscriptions.currency` | string |  |
| `subscriptions.dayOfMonth` | number |  |
| `subscriptions.earliestChargeDateAfterResume` | object |  |
| `subscriptions.endDate` | object |  |
| `subscriptions.id` | string |  |
| `subscriptions.interval` | number |  |
| `subscriptions.intervalUnit` | string |  |
| `subscriptions.links.mandate` | string |  |
| `subscriptions.metadata.source` | string |  |
| `subscriptions.month` | object |  |
| `subscriptions.name` | string |  |
| `subscriptions.parentPlanPaused` | boolean |  |
| `subscriptions.paymentReference` | object |  |
| `subscriptions.retryIfPossible` | boolean |  |
| `subscriptions.startDate` | string |  |
| `subscriptions.status` | string |  |
| `subscriptions.upcomingPayments[].amount` | number |  |
| `subscriptions.upcomingPayments[].chargeDate` | string |  |

## Native endpoint

Through the native GoCardless API, this operation is `POST /subscriptions` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

