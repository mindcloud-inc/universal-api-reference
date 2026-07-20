# Billwerkplus Universal API Examples

These examples use the MindCloud API key and Billwerkplus connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves current account details from Billwerkplus.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/get-current-account?${params}`, {
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
      "country": "string",
      "created": "string",
      "currency": "string",
      "defaultVat": 1,
      "email": "ava@example.com",
      "handle": "string",
      "id": "string",
      "locale": "string",
      "name": "Ava Chen",
      "organisation": "string",
      "state": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-current-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/billwerkplus/latest/actions/get-current-account).

## Cancel Invoice

Cancels an invoice in Billwerkplus.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/cancel-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/cancel-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "amount": 1,
      "amountExVat": 1,
      "amountVat": 1,
      "cancelled": "string",
      "created": "string",
      "currency": "string",
      "customer": "string",
      "discountAmount": 1,
      "due": "string",
      "handle": "string",
      "id": "string",
      "orderLines": [
        {
          "amount": 1,
          "amountDefinedInclVat": true,
          "amountExVat": 1,
          "amountVat": 1,
          "id": "string",
          "ordertext": "string",
          "origin": "string",
          "quantity": 1,
          "timestamp": "string",
          "unitAmount": 1,
          "unitAmountExVat": 1,
          "unitAmountVat": 1,
          "vat": 1
        }
      ],
      "orgAmount": 1,
      "refundedAmount": 1,
      "settledAmount": 1,
      "state": "string",
      "transactions": [
        {
          "amount": 1,
          "created": "string",
          "currency": "string",
          "id": "string",
          "invoice": "string",
          "offlineTransaction": {
            "offlineMandate": {
              "offlineAgreementHandle": "string",
              "offlineAgreementName": "Ava Chen"
            },
            "offlinePaymentInstructions": "string",
            "paymentDueDate": "string"
          },
          "paymentContext": "string",
          "paymentMethod": "string",
          "paymentType": "string",
          "state": "string",
          "type": "string"
        }
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Invoice action reference](actions/cancel-invoice.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/billwerkplus/latest/actions/cancel-invoice).
