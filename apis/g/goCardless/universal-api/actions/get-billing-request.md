# GoCardless: Get Billing Request

Retrieves a single billing request from GoCardless.

```
GET https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/get-billing-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/get-billing-request?connectionId=$CONNECTION_ID&billingRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "billingRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/get-billing-request?${params}`, {
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
| `billingRequestId` | string | yes | ID of the billing request to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingRequests": {
        "autoFulfil": true,
        "createdAt": "string",
        "creditorName": "Ava Chen",
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
        "resources": {
          "customer": {
            "companyName": {},
            "createdAt": "string",
            "email": "ava@example.com",
            "familyName": "Ava Chen",
            "givenName": "Ava Chen",
            "id": "string",
            "language": "string",
            "phoneNumber": {}
          },
          "customerBillingDetail": {
            "addressLine1": "string",
            "addressLine2": {},
            "addressLine3": {},
            "city": "string",
            "countryCode": "string",
            "createdAt": "string",
            "danishIdentityNumber": {},
            "id": "string",
            "postalCode": "string",
            "region": {},
            "swedishIdentityNumber": {}
          }
        },
        "signFlowUrl": {},
        "status": "string",
        "subscriptionRequest": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingRequests.autoFulfil` | boolean |  |
| `billingRequests.createdAt` | string |  |
| `billingRequests.creditorName` | string |  |
| `billingRequests.fallbackEnabled` | boolean |  |
| `billingRequests.fallbackOccurred` | boolean |  |
| `billingRequests.id` | string |  |
| `billingRequests.instalmentScheduleRequest` | object |  |
| `billingRequests.links.creditor` | string |  |
| `billingRequests.links.customer` | string |  |
| `billingRequests.links.customerBillingDetail` | string |  |
| `billingRequests.links.mandateRequest` | string |  |
| `billingRequests.links.organisation` | string |  |
| `billingRequests.links.paymentRequest` | string |  |
| `billingRequests.mandateRequest.consentType` | object |  |
| `billingRequests.mandateRequest.constraints` | object |  |
| `billingRequests.mandateRequest.currency` | string |  |
| `billingRequests.mandateRequest.description` | object |  |
| `billingRequests.mandateRequest.payerRequestedDualSignature` | boolean |  |
| `billingRequests.mandateRequest.scheme` | string |  |
| `billingRequests.mandateRequest.sweeping` | boolean |  |
| `billingRequests.mandateRequest.verify` | string |  |
| `billingRequests.metadata` | object |  |
| `billingRequests.paymentRequest.amount` | number |  |
| `billingRequests.paymentRequest.appFee` | number |  |
| `billingRequests.paymentRequest.currency` | string |  |
| `billingRequests.paymentRequest.defaultMaxAmount` | object |  |
| `billingRequests.paymentRequest.defaultMinAmount` | object |  |
| `billingRequests.paymentRequest.description` | string |  |
| `billingRequests.paymentRequest.flexibleAmount` | boolean |  |
| `billingRequests.paymentRequest.fundsSettlement` | string |  |
| `billingRequests.paymentRequest.maxAmount` | object |  |
| `billingRequests.paymentRequest.minAmount` | object |  |
| `billingRequests.paymentRequest.reference` | object |  |
| `billingRequests.paymentRequest.retryIfPossible` | boolean |  |
| `billingRequests.paymentRequest.scheme` | string |  |
| `billingRequests.resources.customer.companyName` | object |  |
| `billingRequests.resources.customer.createdAt` | string |  |
| `billingRequests.resources.customer.email` | string |  |
| `billingRequests.resources.customer.familyName` | string |  |
| `billingRequests.resources.customer.givenName` | string |  |
| `billingRequests.resources.customer.id` | string |  |
| `billingRequests.resources.customer.language` | string |  |
| `billingRequests.resources.customer.phoneNumber` | object |  |
| `billingRequests.resources.customerBillingDetail.addressLine1` | string |  |
| `billingRequests.resources.customerBillingDetail.addressLine2` | object |  |
| `billingRequests.resources.customerBillingDetail.addressLine3` | object |  |
| `billingRequests.resources.customerBillingDetail.city` | string |  |
| `billingRequests.resources.customerBillingDetail.countryCode` | string |  |
| `billingRequests.resources.customerBillingDetail.createdAt` | string |  |
| `billingRequests.resources.customerBillingDetail.danishIdentityNumber` | object |  |
| `billingRequests.resources.customerBillingDetail.id` | string |  |
| `billingRequests.resources.customerBillingDetail.postalCode` | string |  |
| `billingRequests.resources.customerBillingDetail.region` | object |  |
| `billingRequests.resources.customerBillingDetail.swedishIdentityNumber` | object |  |
| `billingRequests.signFlowUrl` | object |  |
| `billingRequests.status` | string |  |
| `billingRequests.subscriptionRequest` | object |  |

## Native endpoint

Through the native GoCardless API, this operation is `GET /billing_requests/:billingRequestId` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-billing-request.md) for the provider-specific parameters and requirements.

