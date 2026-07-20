# GoCardless: Collect Billing Request Customer Details

Collects customer details for a GoCardless billing request.

```
PUT https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/collect-billing-request-customer-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/collect-billing-request-customer-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "billingRequestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/collect-billing-request-customer-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "billingRequestId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingRequestId` | string | yes | ID of the billing request whose customer details should be collected. |
| `customer` | object | no | Customer fields to collect for the billing request. |
| `customer.email` | string | no | Customer email address. |
| `customer.givenName` | string | no | Customer first name. |
| `customer.familyName` | string | no | Customer surname. |
| `customerBillingDetail` | object | no | Customer billing detail fields to collect for the billing request. |
| `customerBillingDetail.addressLine1` | string | no | First line of the customer's address. |
| `customerBillingDetail.city` | string | no | City of the customer's address. |
| `customerBillingDetail.postalCode` | string | no | Postal code for the customer's address. |
| `customerBillingDetail.countryCode` | string | no | ISO 3166-1 alpha-2 country code. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer.companyName` | string | no | Customer company name. |
| `customer.language` | list<string> | no | ISO 639-1 language code for customer notifications. One of: `0`, `1`, `10`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `customer.phoneNumber` | string | no | Customer phone number in ITU E.123 format. |
| `customer.metadata` | object | no | Key-value store of custom data for the customer. |
| `customerBillingDetail.region` | string | no | Region, county, or department for the address. |
| `customerBillingDetail.ipAddress` | string | no | Payer IP address for ACH customers. |

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

Through the native GoCardless API, this operation is `POST /billing_requests/:billingRequestId/actions/collect_customer_details` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/collect-billing-request-customer-details.md) for the provider-specific parameters and requirements.

