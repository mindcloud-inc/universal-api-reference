# Payrexx: Charge Pre-Authorized Reserved Transaction

Charges a pre-authorized or reserved transaction in Payrexx.

```
PUT https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/charge-pre-authorized-reserved-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payrexx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/charge-pre-authorized-reserved-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "123456"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/charge-pre-authorized-reserved-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "123456"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the transaction to charge. Example: `123456`. |
| `amount` | number | no | Amount for charge in cents. Example: `1000`. |
| `purpose` | string | no | The purpose of the charge. Example: `MindCloud charge test`. |
| `referenceId` | string | no | Reference ID for charged transaction. Example: `mc-charge-001`. |
| `payoutDescriptor` | string | no | Payout descriptor added to the payout statement. Example: `MindCloud Charge`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Payrexx API returns.

## Native endpoint

Through the native Payrexx API, this operation is `POST Transaction/:id/` (base URL `https://api.payrexx.com/v1.14/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/charge-pre-authorized-reserved-transaction.md) for the provider-specific parameters and requirements.

