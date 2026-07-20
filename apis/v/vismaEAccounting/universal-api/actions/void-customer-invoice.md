# Visma eAccounting: Void Customer Invoice

Voids an existing customer invoice in Visma eAccounting.

```
PUT https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/void-customer-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Visma eAccounting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/void-customer-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/void-customer-invoice', {
  method: 'PUT',
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

Through the native Visma eAccounting API, this operation is `POST /customerinvoices/{invoiceId}/void` (base URL `https://eaccountingapi.vismaonline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/void-customer-invoice.md) for the provider-specific parameters and requirements.

