# Column: Reverse ACH Transfer



```
POST https://connect.mindcloud.co/v1/universal/column/latest/actions/reverse-ach-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/column/latest/actions/reverse-ach-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "achTransferId": "string",
  "reason": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/column/latest/actions/reverse-ach-transfer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "achTransferId": "string",
    "reason": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `achTransferId` | string | yes | ID of the original ACH transfer to reverse. |
| `reason` | string | yes | Reason for the ACH reversal. |
| `description` | string | no | Internal description for the reversal transfer. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Column API returns.

## Native endpoint

Through the native Column API, this operation is `POST /transfers/ach/:ach_transfer_id/reverse` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-ach-transfer.md) for the provider-specific parameters and requirements.

