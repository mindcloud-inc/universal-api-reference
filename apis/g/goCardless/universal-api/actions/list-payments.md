# GoCardless: List Payments

Finds payments in your GoCardless account.

```
GET https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-payments?${params}`, {
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
| `createdAt` | object | no | Filter payments by creation time. |
| `createdAt.gt` | date | no | Limit to records created after the specified date-time. |
| `createdAt.gte` | date | no | Limit to records created on or after the specified date-time. |
| `createdAt.lt` | date | no | Limit to records created before the specified date-time. |
| `createdAt.lte` | date | no | Limit to records created on or before the specified date-time. |
| `creditor` | string | no | Filter payments to a specific creditor. |
| `customer` | string | no | Filter payments to a specific customer. |
| `mandate` | string | no | Filter payments to a specific mandate. |
| `status` | string | no | Filter payments by status. |
| `subscription` | string | no | Filter payments to a specific subscription. |
| `sortDirection` | string | no | Control the sort direction for the returned payments. |

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
      "payments": [
        {
          "amount": 1,
          "amountRefunded": 1,
          "chargeDate": "string",
          "createdAt": "string",
          "currency": "string",
          "description": {},
          "fx": {
            "estimatedExchangeRate": {},
            "exchangeRate": {},
            "fxAmount": {},
            "fxCurrency": {}
          },
          "id": "string",
          "links": {
            "creditor": "https://example.com",
            "mandate": "https://example.com"
          },
          "reference": {},
          "retryIfPossible": true,
          "scheme": "string",
          "status": "string"
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
| `payments[].amount` | number |  |
| `payments[].amountRefunded` | number |  |
| `payments[].chargeDate` | string |  |
| `payments[].createdAt` | string |  |
| `payments[].currency` | string |  |
| `payments[].description` | object |  |
| `payments[].fx.estimatedExchangeRate` | object |  |
| `payments[].fx.exchangeRate` | object |  |
| `payments[].fx.fxAmount` | object |  |
| `payments[].fx.fxCurrency` | object |  |
| `payments[].id` | string |  |
| `payments[].links.creditor` | string |  |
| `payments[].links.mandate` | string |  |
| `payments[].reference` | object |  |
| `payments[].retryIfPossible` | boolean |  |
| `payments[].scheme` | string |  |
| `payments[].status` | string |  |

## Native endpoint

Through the native GoCardless API, this operation is `GET /payments` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

