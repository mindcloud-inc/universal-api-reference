# GoCardless: List Billing Requests

Finds billing requests in your GoCardless account.

```
GET https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-billing-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-billing-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-billing-requests?${params}`, {
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
| `customer` | string | no | ID of the customer. If specified, this endpoint returns billing requests for that customer. |
| `status` | list<string> | no | Status of the billing request. One of: `0`, `1`, `2`, `3`, `4`. |
| `createdAt` | date | no | Fixed timestamp recording when this resource was created. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingRequests": [
        {
          "autoFulfil": true,
          "createdAt": "string",
          "fallbackEnabled": true,
          "fallbackOccurred": true,
          "id": "string",
          "instalmentScheduleRequest": {},
          "links": {
            "creditor": "https://example.com",
            "customer": "https://example.com",
            "customerBillingDetail": "https://example.com",
            "mandateRequest": "https://example.com",
            "organisation": "https://example.com",
            "paymentRequest": "https://example.com"
          },
          "mandateRequest": {
            "consentType": {},
            "constraints": {},
            "currency": "string",
            "description": {},
            "payerRequestedDualSignature": true,
            "scheme": "string",
            "sweeping": true,
            "verify": "string"
          },
          "metadata": {},
          "paymentRequest": {
            "amount": 1,
            "appFee": 1,
            "currency": "string",
            "defaultMaxAmount": {},
            "defaultMinAmount": {},
            "description": "string",
            "flexibleAmount": true,
            "fundsSettlement": "string",
            "maxAmount": {},
            "minAmount": {},
            "reference": {},
            "retryIfPossible": true,
            "scheme": "string"
          },
          "signFlowUrl": {},
          "status": "string",
          "subscriptionRequest": {}
        }
      ],
      "meta": {
        "cursors": {
          "after": {},
          "before": {}
        },
        "limit": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingRequests[].autoFulfil` | boolean |  |
| `billingRequests[].createdAt` | string |  |
| `billingRequests[].fallbackEnabled` | boolean |  |
| `billingRequests[].fallbackOccurred` | boolean |  |
| `billingRequests[].id` | string |  |
| `billingRequests[].instalmentScheduleRequest` | object |  |
| `billingRequests[].links.creditor` | string |  |
| `billingRequests[].links.customer` | string |  |
| `billingRequests[].links.customerBillingDetail` | string |  |
| `billingRequests[].links.mandateRequest` | string |  |
| `billingRequests[].links.organisation` | string |  |
| `billingRequests[].links.paymentRequest` | string |  |
| `billingRequests[].mandateRequest.consentType` | object |  |
| `billingRequests[].mandateRequest.constraints` | object |  |
| `billingRequests[].mandateRequest.currency` | string |  |
| `billingRequests[].mandateRequest.description` | object |  |
| `billingRequests[].mandateRequest.payerRequestedDualSignature` | boolean |  |
| `billingRequests[].mandateRequest.scheme` | string |  |
| `billingRequests[].mandateRequest.sweeping` | boolean |  |
| `billingRequests[].mandateRequest.verify` | string |  |
| `billingRequests[].metadata` | object |  |
| `billingRequests[].paymentRequest.amount` | number |  |
| `billingRequests[].paymentRequest.appFee` | number |  |
| `billingRequests[].paymentRequest.currency` | string |  |
| `billingRequests[].paymentRequest.defaultMaxAmount` | object |  |
| `billingRequests[].paymentRequest.defaultMinAmount` | object |  |
| `billingRequests[].paymentRequest.description` | string |  |
| `billingRequests[].paymentRequest.flexibleAmount` | boolean |  |
| `billingRequests[].paymentRequest.fundsSettlement` | string |  |
| `billingRequests[].paymentRequest.maxAmount` | object |  |
| `billingRequests[].paymentRequest.minAmount` | object |  |
| `billingRequests[].paymentRequest.reference` | object |  |
| `billingRequests[].paymentRequest.retryIfPossible` | boolean |  |
| `billingRequests[].paymentRequest.scheme` | string |  |
| `billingRequests[].signFlowUrl` | object |  |
| `billingRequests[].status` | string |  |
| `billingRequests[].subscriptionRequest` | object |  |
| `meta.cursors.after` | object |  |
| `meta.cursors.before` | object |  |
| `meta.limit` | number |  |

## Native endpoint

Through the native GoCardless API, this operation is `GET /billing_requests` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-billing-requests.md) for the provider-specific parameters and requirements.

