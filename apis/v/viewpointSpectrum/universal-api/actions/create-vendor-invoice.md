# Viewpoint Spectrum: Create Vendor Invoice



```
POST https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-vendor-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-vendor-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batchCode": "string",
  "gLDate": "string",
  "invoiceAmount": 1,
  "invoiceDate": "2026-05-07T12:00:00.000Z",
  "invoiceNumber": "string",
  "invoiceTypeCode": "string",
  "vendorCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-vendor-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batchCode": "string",
    "gLDate": "string",
    "invoiceAmount": 1,
    "invoiceDate": "2026-05-07T12:00:00.000Z",
    "invoiceNumber": "string",
    "invoiceTypeCode": "string",
    "vendorCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aPGLAccount` | string | no |  |
| `batchCode` | string | yes |  |
| `contractNumber` | string | no |  |
| `costType` | string | no |  |
| `discountAmount` | number | no |  |
| `discountDueDate` | date | no |  |
| `distributionGLAccount` | string | no |  |
| `equipmentCategory` | string | no |  |
| `equipmentCode` | string | no |  |
| `equipmentWorkOrder` | string | no |  |
| `expenseCostCenter` | string | no |  |
| `gLDate` | string | yes |  |
| `invoiceAmount` | number | yes |  |
| `invoiceDate` | date | yes |  |
| `invoiceNumber` | string | yes |  |
| `invoiceTypeCode` | list | yes |  |
| `itemCode` | string | no |  |
| `jobNumber` | string | no |  |
| `liabilityCostCenter` | string | no |  |
| `paymentDueDate` | date | no |  |
| `phaseCode` | string | no |  |
| `pONumber` | string | no |  |
| `quantity` | number | no |  |
| `remarks` | string | no |  |
| `retentionAmount` | number | no |  |
| `salesTaxAmount` | number | no |  |
| `status` | list | no |  |
| `taxCode` | string | no |  |
| `totalVATAmt` | number | no |  |
| `vATCode` | string | no |  |
| `vendorCode` | string | yes |  |
| `wOComponent` | string | no |  |
| `wOEquipment` | string | no |  |
| `wONumber` | string | no |  |
| `wOSCContract` | string | no |  |
| `wOUnitPrice` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST ws/AddAPInvoice` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor-invoice.md) for the provider-specific parameters and requirements.

