# Aspire: Approve Receipt

Approves an existing Aspire receipt and can optionally receive it at the same time. This is the only post-create update path for a receipt. At approve time, the only receipt fields that can be added or changed are the vendor invoice number and vendor invoice date. No other receipt field can be edited through this action, including notes, extra costs or freight, receipt items, received date, vendor, branch, or work ticket. If the user asks to change a non-invoice-metadata field on an existing receipt, surface that limitation upfront and offer the available path of recreating the receipt with the corrected values.

```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/approve-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/approve-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/approve-receipt', {
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
| `Receive` | boolean | no |  |
| `VendorInvoiceNum` | string | no |  |
| `VendorInvoiceDate` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aspire API returns.

## Native endpoint

Through the native Aspire API, this operation is `POST Receipts/Approve` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-receipt.md) for the provider-specific parameters and requirements.

