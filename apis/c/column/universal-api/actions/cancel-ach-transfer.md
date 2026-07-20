# Column: Cancel ACH Transfer



```
PUT https://connect.mindcloud.co/v1/universal/column/latest/actions/cancel-ach-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/column/latest/actions/cancel-ach-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "achTransferId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/column/latest/actions/cancel-ach-transfer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "achTransferId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `achTransferId` | string | yes | ID of the ACH transfer to cancel. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Column API returns.

## Native endpoint

Through the native Column API, this operation is `POST /transfers/ach/:ach_transfer_id/cancel` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-ach-transfer.md) for the provider-specific parameters and requirements.

