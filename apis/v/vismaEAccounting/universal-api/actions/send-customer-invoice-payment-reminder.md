# Visma eAccounting: Send Customer Invoice Payment Reminder

Creates a payment reminder for a customer invoice in Visma eAccounting.

```
POST https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/send-customer-invoice-payment-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Visma eAccounting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/send-customer-invoice-payment-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/send-customer-invoice-payment-reminder', {
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



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Visma eAccounting API returns.

## Native endpoint

Through the native Visma eAccounting API, this operation is `POST /customerinvoices/{invoiceId}/paymentreminders` (base URL `https://eaccountingapi.vismaonline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-customer-invoice-payment-reminder.md) for the provider-specific parameters and requirements.

