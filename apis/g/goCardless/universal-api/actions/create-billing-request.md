# GoCardless: Create Billing Request

Creates a new billing request in GoCardless.

```
POST https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-billing-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-billing-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-billing-request', {
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
| `paymentRequest` | object | no | Payment request payload for the billing request. |
| `paymentRequest.description` | string | no | Human-readable description displayed to the payer. |
| `paymentRequest.amount` | number | no | Amount in minor units. |
| `paymentRequest.currency` | list<string> | no | ISO 4217 currency code for the payment request. One of: `0`, `1`. |
| `mandateRequest` | object | no | Mandate request payload for the billing request. |
| `mandateRequest.scheme` | list<string> | no | Bank payment scheme for the mandate request. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `mandateRequest.verify` | list<string> | no | Verification preference for the mandate request. One of: `0`, `1`, `2`, `3`. |
| `links` | object | no | Related resource identifiers for this billing request. |
| `links.customer` | string | no | ID of the customer against which this request should be made. |
| `links.customerBankAccount` | string | no | ID of the customer bank account against which this request should be made. |
| `links.creditor` | string | no | ID of the associated creditor. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fallbackEnabled` | boolean | no | If true, this billing request can fallback from instant payment to direct debit. |
| `metadata` | object | no | Key-value store of custom data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingRequests": {
        "actions": [
          {
            "availableCurrencies": [
              "string"
            ],
            "required": true,
            "status": "string",
            "type": "string"
          }
        ],
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
          "customerBankAccount": "https://example.com",
          "customerBillingDetail": "https://example.com",
          "mandateRequest": "https://example.com",
          "organisation": "https://example.com"
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
        "paymentRequest": {},
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
          "customerBankAccount": {
            "accountHolderName": "Ava Chen",
            "accountNumberEnding": "string",
            "accountType": {},
            "bankName": "Ava Chen",
            "branchCodeEnding": "string",
            "countryCode": "string",
            "createdAt": "string",
            "currency": "string",
            "enabled": true,
            "id": "string",
            "links": {
              "customer": "https://example.com"
            }
          },
          "customerBillingDetail": {
            "addressLine1": {},
            "addressLine2": {},
            "addressLine3": {},
            "city": {},
            "countryCode": {},
            "createdAt": "string",
            "danishIdentityNumber": {},
            "id": "string",
            "postalCode": {},
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
| `billingRequests.actions[].availableCurrencies[]` | string |  |
| `billingRequests.actions[].required` | boolean |  |
| `billingRequests.actions[].status` | string |  |
| `billingRequests.actions[].type` | string |  |
| `billingRequests.autoFulfil` | boolean |  |
| `billingRequests.createdAt` | string |  |
| `billingRequests.creditorName` | string |  |
| `billingRequests.fallbackEnabled` | boolean |  |
| `billingRequests.fallbackOccurred` | boolean |  |
| `billingRequests.id` | string |  |
| `billingRequests.instalmentScheduleRequest` | object |  |
| `billingRequests.links.creditor` | string |  |
| `billingRequests.links.customer` | string |  |
| `billingRequests.links.customerBankAccount` | string |  |
| `billingRequests.links.customerBillingDetail` | string |  |
| `billingRequests.links.mandateRequest` | string |  |
| `billingRequests.links.organisation` | string |  |
| `billingRequests.mandateRequest.consentType` | object |  |
| `billingRequests.mandateRequest.constraints` | object |  |
| `billingRequests.mandateRequest.currency` | string |  |
| `billingRequests.mandateRequest.description` | object |  |
| `billingRequests.mandateRequest.payerRequestedDualSignature` | boolean |  |
| `billingRequests.mandateRequest.scheme` | string |  |
| `billingRequests.mandateRequest.sweeping` | boolean |  |
| `billingRequests.mandateRequest.verify` | string |  |
| `billingRequests.metadata` | object |  |
| `billingRequests.paymentRequest` | object |  |
| `billingRequests.resources.customer.companyName` | object |  |
| `billingRequests.resources.customer.createdAt` | string |  |
| `billingRequests.resources.customer.email` | string |  |
| `billingRequests.resources.customer.familyName` | string |  |
| `billingRequests.resources.customer.givenName` | string |  |
| `billingRequests.resources.customer.id` | string |  |
| `billingRequests.resources.customer.language` | string |  |
| `billingRequests.resources.customer.phoneNumber` | object |  |
| `billingRequests.resources.customerBankAccount.accountHolderName` | string |  |
| `billingRequests.resources.customerBankAccount.accountNumberEnding` | string |  |
| `billingRequests.resources.customerBankAccount.accountType` | object |  |
| `billingRequests.resources.customerBankAccount.bankName` | string |  |
| `billingRequests.resources.customerBankAccount.branchCodeEnding` | string |  |
| `billingRequests.resources.customerBankAccount.countryCode` | string |  |
| `billingRequests.resources.customerBankAccount.createdAt` | string |  |
| `billingRequests.resources.customerBankAccount.currency` | string |  |
| `billingRequests.resources.customerBankAccount.enabled` | boolean |  |
| `billingRequests.resources.customerBankAccount.id` | string |  |
| `billingRequests.resources.customerBankAccount.links.customer` | string |  |
| `billingRequests.resources.customerBillingDetail.addressLine1` | object |  |
| `billingRequests.resources.customerBillingDetail.addressLine2` | object |  |
| `billingRequests.resources.customerBillingDetail.addressLine3` | object |  |
| `billingRequests.resources.customerBillingDetail.city` | object |  |
| `billingRequests.resources.customerBillingDetail.countryCode` | object |  |
| `billingRequests.resources.customerBillingDetail.createdAt` | string |  |
| `billingRequests.resources.customerBillingDetail.danishIdentityNumber` | object |  |
| `billingRequests.resources.customerBillingDetail.id` | string |  |
| `billingRequests.resources.customerBillingDetail.postalCode` | object |  |
| `billingRequests.resources.customerBillingDetail.region` | object |  |
| `billingRequests.resources.customerBillingDetail.swedishIdentityNumber` | object |  |
| `billingRequests.signFlowUrl` | object |  |
| `billingRequests.status` | string |  |
| `billingRequests.subscriptionRequest` | object |  |

## Native endpoint

Through the native GoCardless API, this operation is `POST /billing_requests` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-billing-request.md) for the provider-specific parameters and requirements.

