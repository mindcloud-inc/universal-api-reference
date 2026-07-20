# Aspire: Receive Receipt

Marks an existing Aspire receipt as received. This action accepts the receipt identifier only and does not perform receipt-level edits. It cannot set or change invoice metadata, notes, extra costs or freight, receipt items, received date, or any other receipt field. If the user wants to record vendor invoice number or vendor invoice date around the same workflow, use approveReceipt because approveReceipt is the only post-create path for those two fields. For any other requested change to an existing receipt, explain that Aspire has no updateReceipt or patch action and the receipt must be recreated with the correct values.

```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/receive-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/receive-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/receive-receipt', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ReceiptID` | list<number> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aspire API returns.

## Native endpoint

Through the native Aspire API, this operation is `POST Receipts/Receive` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/receive-receipt.md) for the provider-specific parameters and requirements.

