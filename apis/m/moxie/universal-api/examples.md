# Moxie Universal API Examples

These examples use the MindCloud API key and Moxie connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspace Users

Retrieves workspace users from Moxie.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/list-workspace-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moxie/latest/actions/list-workspace-users?${params}`, {
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
      "user": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "phoneVerified": true,
        "pricingVersion": 1,
        "uploadedPicture": true,
        "userAccounts": [
          {
            "account": {
              "accountId": 1,
              "accountName": "Ava Chen",
              "disabled": true,
              "free": true,
              "inTrial": true,
              "ltd": true,
              "paid": true,
              "pod": {
                "podId": "string",
                "podUrl": "https://example.com"
              },
              "pricingVersion": 1,
              "restricted": true,
              "sampleMode": true,
              "starter": true,
              "subscriptionProvider": "string",
              "subscriptionState": "string",
              "subscriptionType": "string",
              "trialEndsAt": "2026-05-07T12:00:00.000Z"
            },
            "userType": "string"
          }
        ],
        "userId": 1,
        "uuid": "string"
      },
      "userType": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Workspace Users action reference](actions/list-workspace-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moxie/latest/actions/list-workspace-users).

## Apply Payment to Invoice

Applies a payment to an invoice in Moxie.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/apply-payment-to-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "date": "2026-03-15",
  "amount": 1,
  "invoiceNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moxie/latest/actions/apply-payment-to-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "date": "2026-03-15",
    "amount": 1,
    "invoiceNumber": "string"
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
      "accountId": 1,
      "amountDue": 1,
      "clientId": "string",
      "clientInfo": {},
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "datePaid": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "invoiceNumber": 1,
      "invoiceNumberFormatted": "string",
      "payments": [
        {}
      ],
      "paymentTotal": 1,
      "status": "string",
      "total": 1,
      "viewOnlineUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Apply Payment to Invoice action reference](actions/apply-payment-to-invoice.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moxie/latest/actions/apply-payment-to-invoice).
