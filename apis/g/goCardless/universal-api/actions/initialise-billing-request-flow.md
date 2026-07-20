# GoCardless: Initialise Billing Request Flow

Initialises a GoCardless billing request flow.

```
PUT https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/initialise-billing-request-flow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/initialise-billing-request-flow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "billingRequestFlowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/initialise-billing-request-flow', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "billingRequestFlowId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingRequestFlowId` | string | yes | ID of the billing request flow to initialise. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingRequestFlows": {
        "authorisationUrl": "https://example.com",
        "autoFulfil": true,
        "config": {
          "merchantContactDetails": {
            "email": "ava@example.com",
            "name": "Ava Chen",
            "phoneNumber": {},
            "url": {}
          },
          "schemeIdentifiers": [
            {
              "address": "string",
              "advanceNotice": 1,
              "bankStatementName": "Ava Chen",
              "name": "Ava Chen",
              "reference": "string",
              "registeredName": "Ava Chen",
              "scheme": "string"
            }
          ]
        },
        "createdAt": "string",
        "customerDetailsCaptured": true,
        "exitUri": "string",
        "expiresAt": "string",
        "id": "string",
        "language": {},
        "links": {
          "billingRequest": "https://example.com"
        },
        "lockBankAccount": true,
        "lockCurrency": true,
        "lockCustomerDetails": true,
        "prefilledBankAccount": {},
        "prefilledCustomer": {
          "email": "ava@example.com",
          "familyName": "Ava Chen",
          "givenName": "Ava Chen"
        },
        "redirectFlowId": {},
        "redirectOrigin": {},
        "redirectUri": "string",
        "sessionToken": "string",
        "showRedirectButtons": true,
        "showSuccessRedirectButton": true,
        "skipSuccessScreen": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingRequestFlows.authorisationUrl` | string |  |
| `billingRequestFlows.autoFulfil` | boolean |  |
| `billingRequestFlows.config.merchantContactDetails.email` | string |  |
| `billingRequestFlows.config.merchantContactDetails.name` | string |  |
| `billingRequestFlows.config.merchantContactDetails.phoneNumber` | object |  |
| `billingRequestFlows.config.merchantContactDetails.url` | object |  |
| `billingRequestFlows.config.schemeIdentifiers[].address` | string |  |
| `billingRequestFlows.config.schemeIdentifiers[].advanceNotice` | number |  |
| `billingRequestFlows.config.schemeIdentifiers[].bankStatementName` | string |  |
| `billingRequestFlows.config.schemeIdentifiers[].name` | string |  |
| `billingRequestFlows.config.schemeIdentifiers[].reference` | string |  |
| `billingRequestFlows.config.schemeIdentifiers[].registeredName` | string |  |
| `billingRequestFlows.config.schemeIdentifiers[].scheme` | string |  |
| `billingRequestFlows.createdAt` | string |  |
| `billingRequestFlows.customerDetailsCaptured` | boolean |  |
| `billingRequestFlows.exitUri` | string |  |
| `billingRequestFlows.expiresAt` | string |  |
| `billingRequestFlows.id` | string |  |
| `billingRequestFlows.language` | object |  |
| `billingRequestFlows.links.billingRequest` | string |  |
| `billingRequestFlows.lockBankAccount` | boolean |  |
| `billingRequestFlows.lockCurrency` | boolean |  |
| `billingRequestFlows.lockCustomerDetails` | boolean |  |
| `billingRequestFlows.prefilledBankAccount` | object |  |
| `billingRequestFlows.prefilledCustomer.email` | string |  |
| `billingRequestFlows.prefilledCustomer.familyName` | string |  |
| `billingRequestFlows.prefilledCustomer.givenName` | string |  |
| `billingRequestFlows.redirectFlowId` | object |  |
| `billingRequestFlows.redirectOrigin` | object |  |
| `billingRequestFlows.redirectUri` | string |  |
| `billingRequestFlows.sessionToken` | string |  |
| `billingRequestFlows.showRedirectButtons` | boolean |  |
| `billingRequestFlows.showSuccessRedirectButton` | boolean |  |
| `billingRequestFlows.skipSuccessScreen` | boolean |  |

## Native endpoint

Through the native GoCardless API, this operation is `POST /billing_request_flows/:billingRequestFlowId/actions/initialise` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initialise-billing-request-flow.md) for the provider-specific parameters and requirements.

