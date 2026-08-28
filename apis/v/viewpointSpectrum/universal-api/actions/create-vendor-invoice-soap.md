# Viewpoint Spectrum: Create Vendor Invoice (SOAP)



```
POST https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-vendor-invoice-soap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-vendor-invoice-soap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vendorCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-vendor-invoice-soap', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vendorCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batchCode` | string | no |  |
| `vendorCode` | string | yes |  |
| `GL_Date` | string | no |  |
| `contractNumber` | string | no |  |
| `invoiceNumber` | string | no |  |
| `invoiceTypeCode` | string | no |  |
| `invoiceDate` | string | no |  |
| `invoiceAmount` | string | no |  |
| `salesTaxAmount` | string | no |  |
| `retentionAmount` | string | no |  |
| `paymentDueDate` | string | no |  |
| `status` | string | no |  |
| `discountDueDate` | string | no |  |
| `discountAmount` | string | no |  |
| `remarks` | string | no |  |
| `apGlAccount` | string | no |  |
| `distributionGlAccount` | string | no |  |
| `jobNumber` | string | no |  |
| `phaseCode` | string | no |  |
| `costType` | string | no |  |
| `equipmentCode` | string | no |  |
| `equipmentCategory` | string | no |  |
| `equipmentWorkOrder` | string | no |  |
| `woNumber` | string | no |  |
| `itemCode` | string | no |  |
| `quantity` | string | no |  |
| `woEquipment` | string | no |  |
| `woComponent` | string | no |  |
| `woServiceContract` | string | no |  |
| `woUnitPrice` | string | no |  |
| `taxCode` | string | no |  |
| `vatCode` | string | no |  |
| `totalVatAmount` | string | no |  |
| `liabilityCostCenter` | string | no |  |
| `expenseCostCenter` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST ws/AddAPInvoice` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor-invoice-soap.md) for the provider-specific parameters and requirements.

