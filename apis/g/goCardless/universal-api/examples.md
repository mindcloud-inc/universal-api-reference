# GoCardless Universal API Examples

These examples use the MindCloud API key and GoCardless connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Billing Request

Retrieves a single billing request from GoCardless.

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

Example response:

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

See the full [Get Billing Request action reference](actions/get-billing-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goCardless/latest/actions/get-billing-request).

## Cancel Billing Request

Cancels an existing billing request in GoCardless.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/cancel-billing-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "billingRequestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/cancel-billing-request', {
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

Example response:

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

See the full [Cancel Billing Request action reference](actions/cancel-billing-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goCardless/latest/actions/cancel-billing-request).
