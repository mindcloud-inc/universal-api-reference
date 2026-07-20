# Viewpoint Spectrum: Create Customer Invoice



```
POST https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-customer-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-customer-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "gLDate": "string",
  "batchCode": "string",
  "customerCode": "string",
  "transactionType": "string",
  "invoiceDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-customer-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "gLDate": "string",
    "batchCode": "string",
    "customerCode": "string",
    "transactionType": "string",
    "invoiceDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `gLDate` | string | yes |  |
| `batchCode` | string | yes |  |
| `customerCode` | string | yes |  |
| `jobNumber` | string | no |  |
| `invoiceOrTransaction` | string | no |  |
| `transactionType` | list | yes |  |
| `invoiceDate` | date | yes |  |
| `termsCode` | string | no |  |
| `salespersonCode` | number | no |  |
| `salesTaxCode` | number | no |  |
| `taxableFlag` | string | no |  |
| `retentionPercent` | string | no |  |
| `printJobAddressFlag` | string | no |  |
| `remarks` | string | no |  |
| `customerPO` | string | no |  |
| `aRGLAccount` | string | no |  |
| `detailDescription` | string | no |  |
| `lineExtension` | string | no |  |
| `gLAccount` | string | no |  |
| `salesTaxAmount` | number | no |  |
| `retentionAmount` | string | no |  |
| `vATCode` | string | no |  |
| `totalVATAmt` | number | no |  |
| `assetCostCenter` | string | no |  |
| `incomeCostCenter` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST ws/AddARInvoice` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-invoice.md) for the provider-specific parameters and requirements.

