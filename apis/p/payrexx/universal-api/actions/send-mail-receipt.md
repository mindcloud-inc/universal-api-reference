# Payrexx: Send Mail Receipt

Sends a transaction receipt email from Payrexx.

```
PUT https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/send-mail-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payrexx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/send-mail-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "123456",
  "recipient": "buyer@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/send-mail-receipt', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "123456",
    "recipient": "buyer@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the transaction with a receipt. Example: `123456`. |
| `recipient` | string | yes | Email address of recipient. Example: `buyer@example.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Payrexx API returns.

## Native endpoint

Through the native Payrexx API, this operation is `POST Transaction/:id/receipt` (base URL `https://api.payrexx.com/v1.14/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-mail-receipt.md) for the provider-specific parameters and requirements.

