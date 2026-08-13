# Viewpoint Vista: Add Receipt Batch Entry



```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-receipt-batch-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-receipt-batch-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "co": 1,
  "mth": "string",
  "batchId": 1,
  "customer": 1,
  "creditAmt": "string",
  "cmDeposit": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-receipt-batch-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "co": 1,
    "mth": "string",
    "batchId": 1,
    "customer": 1,
    "creditAmt": "string",
    "cmDeposit": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `co` | number | yes | Key to ar/batches(Co, Mth, BatchId). |
| `mth` | string | yes | Key to ar/batches(Co, Mth, BatchId). Format: YYYY-MM-01. |
| `batchId` | number | yes | Key to ar/batches(Co, Mth, BatchId). |
| `customer` | number | yes | Key to ar/customers(CustGroup, Customer). CustGroup is defaulted based on Co. |
| `transDate` | string | no | Transaction date. Format: YYYY-MM-DD. Optional; defaults to today. |
| `checkNo` | string | no | Check number. Optional. |
| `checkDate` | string | no | Check date. Format: YYYY-MM-DD. Optional. |
| `creditAmt` | string | yes | Check amount. |
| `cmCo` | number | no | CM company. Optional; defaults based on AR company settings. |
| `cmAcct` | number | no | CM account. Optional; defaults based on AR company settings. |
| `cmDeposit` | string | yes | Deposit number. |
| `notes` | string | no | Optional notes. |
| `customFields` | object | no | User-defined values to set on the batch transaction header. |
| `miscDistributions[]` | array<object> | no | Optional misc distribution rows for the receipt. |
| `LineItems[]` | array<object> | no | Optional receipt application rows. |
| `miscDistributions[].miscDistCode` | string | no | Misc distribution code. |
| `miscDistributions[].distDate` | date | no | Distribution date. Format: YYYY-MM-DD. |
| `miscDistributions[].description` | string | no | Optional misc distribution description. |
| `miscDistributions[].amount` | string | no | Misc distribution amount. |
| `miscDistributions[].customFields` | object | no | User-defined values to set on the misc distribution. |
| `LineItems[].arLine` | number | no | Optional line number. If omitted, Vista defaults the next ARLine number. |
| `LineItems[].lineType` | list<string> | no | C applies payment to an invoice line. A applies funds on account. One of: `A`, `C`. |
| `LineItems[].applyMth` | date | no | Reference month for the transaction line being paid or for previously saved on-account funds. Format: YYYY-MM-01. |
| `LineItems[].applyTrans` | number | no | Reference transaction being paid or prior on-account receipt transaction. |
| `LineItems[].applyLine` | number | no | Reference transaction line being paid or prior on-account receipt line. |
| `LineItems[].amount` | string | no | Amount applied for this line item or on-account adjustment amount. |
| `LineItems[].discTaken` | string | no | Optional discount amount to take on this line item. |
| `LineItems[].taxAmount` | string | no | Optional tax amount applied to an invoice line item. |
| `LineItems[].retainage` | string | no | Optional retainage amount applied to an invoice line item. |
| `LineItems[].notes` | string | no | Optional line-item notes. |
| `LineItems[].customFields` | object | no | User-defined values to set on the receipt line item. |
| `LineItems[].recType` | number | no | Receivable type for on-account line items. Optional. |
| `LineItems[].description` | string | no | Optional description for on-account line items. |
| `LineItems[].tax` | object | no | Optional tax details for on-account line items. |
| `LineItems[].tax.taxCode` | string | no | Optional tax code for on-account line items. |
| `LineItems[].tax.taxBasis` | string | no | Optional tax basis amount for on-account line items. |
| `LineItems[].tax.taxAmount` | string | no | Optional tax amount for on-account line items. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/batch_entries/actions/add_receipt` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-receipt-batch-entry.md) for the provider-specific parameters and requirements.

