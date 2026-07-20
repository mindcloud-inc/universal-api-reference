# Rillion Prime: Update Invoice Queue Transfer Flag



```
PUT https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-invoice-queue-transfer-flag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-invoice-queue-transfer-flag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transfer": true,
  "role": "Administrator"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-invoice-queue-transfer-flag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transfer": true,
    "role": "Administrator"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transfer` | boolean | yes | Path value for Transfer. |
| `role` | string | yes | Path value for Role. Example: `Administrator`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `POST /invoicequeue/updatetransferflag/transfer/:transfer/role/:role` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice-queue-transfer-flag.md) for the provider-specific parameters and requirements.

