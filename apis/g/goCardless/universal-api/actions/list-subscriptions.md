# GoCardless: List Subscriptions

Finds subscriptions in your GoCardless account.

```
GET https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-subscriptions?${params}`, {
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
| `createdAt` | object | no |  |
| `createdAt.gt` | date | no |  |
| `createdAt.gte` | date | no |  |
| `createdAt.lt` | date | no |  |
| `createdAt.lte` | date | no |  |
| `customer` | string | no |  |
| `mandate` | string | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "cursors": {
          "after": {},
          "before": {}
        },
        "limit": 1
      },
      "subscriptions": [
        {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.cursors.after` | object |  |
| `meta.cursors.before` | object |  |
| `meta.limit` | number |  |
| `subscriptions[].amount` | number |  |
| `subscriptions[].appFee` | number |  |
| `subscriptions[].count` | object |  |
| `subscriptions[].createdAt` | string |  |
| `subscriptions[].currency` | string |  |
| `subscriptions[].dayOfMonth` | number |  |
| `subscriptions[].earliestChargeDateAfterResume` | object |  |
| `subscriptions[].endDate` | object |  |
| `subscriptions[].id` | string |  |
| `subscriptions[].interval` | number |  |
| `subscriptions[].intervalUnit` | string |  |
| `subscriptions[].links.mandate` | string |  |
| `subscriptions[].metadata.source` | string |  |
| `subscriptions[].month` | object |  |
| `subscriptions[].name` | string |  |
| `subscriptions[].parentPlanPaused` | boolean |  |
| `subscriptions[].paymentReference` | object |  |
| `subscriptions[].retryIfPossible` | boolean |  |
| `subscriptions[].startDate` | string |  |
| `subscriptions[].status` | string |  |
| `subscriptions[].upcomingPayments[].amount` | number |  |
| `subscriptions[].upcomingPayments[].chargeDate` | string |  |

## Native endpoint

Through the native GoCardless API, this operation is `GET /subscriptions` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

