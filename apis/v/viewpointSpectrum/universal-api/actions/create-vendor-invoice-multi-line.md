# Viewpoint Spectrum: Create Vendor Invoice Multi-Line



```
POST https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-vendor-invoice-multi-line
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-vendor-invoice-multi-line" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-vendor-invoice-multi-line', {
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
| `APInvoiceDetails[].Amount` | number | no |  |
| `APInvoiceDetails[].Distribution.Cost_Center` | string | no |  |
| `APInvoiceDetails[].Distribution.GL_Account` | string | no |  |
| `APInvoiceDetails[].Equipment.Equipment_Category` | string | no |  |
| `APInvoiceDetails[].Equipment.Equipment_Code` | string | no |  |
| `APInvoiceDetails[].Item_Description` | string | no |  |
| `APInvoiceDetails[].Job` | object | no |  |
| `APInvoiceDetails[].Job.Cost_Type` | string | no |  |
| `APInvoiceDetails[].Job.Phase_Code` | string | no |  |
| `APInvoiceDetails[].Quantity` | number | no |  |
| `APInvoiceDetails[].Tax_Code` | string | no |  |
| `APInvoiceDetails[].Unit_Of_Measure` | string | no |  |
| `APInvoiceDetails[].Work_Order.Component` | string | no |  |
| `APInvoiceDetails[].Work_Order.Equipment` | string | no |  |
| `APInvoiceDetails[].Work_Order.Service_Contract` | string | no |  |
| `APInvoiceDetails[].Work_Order.Unit_Price` | number | no |  |
| `Images[].Document_ID` | string | no |  |
| `Images[].Image_Description` | string | no |  |
| `Images[].Image_File` | string | no | Base64 |
| `APInvoiceDetails[].Distribution` | object | no |  |
| `APInvoiceDetails[].Distribution.Company_Code` | string | no |  |
| `APInvoiceDetails[].Equipment.Equipment_Work_Order` | string | no |  |
| `APInvoiceDetails[].Job.Job_Number` | string | no |  |
| `APInvoiceDetails[].Work_Order.WO_Number` | string | no |  |
| `Images[].Image_Type` | string | no |  |
| `Invoice_Number` | string | no |  |
| `APInvoiceDetails[].Item_Code` | string | no |  |
| `Vendor_Code` | string | no |  |
| `Approval_Status` | string | no |  |
| `Invoice_Type_Code` | string | no | I — Invoice [default] C — Credit memo |
| `Routing_Code` | string | no |  |
| `GL_Date` | string | no | Eg: 05/15/2017 |
| `Invoice_Date` | string | no |  |
| `Invoice_Amount` | number | no |  |
| `APInvoiceDetails[].Equipment` | object | no |  |
| `Sales_Tax_Amount` | number | no |  |
| `APInvoiceDetails[].Work_Order` | object | no |  |
| `VAT_Code` | string | no |  |
| `APInvoiceDetails[].Remark` | string | no |  |
| `Total_VAT_Amount` | string | no |  |
| `Contract_Number` | string | no |  |
| `Retention_Amount` | number | no |  |
| `Batch_Code` | string | no |  |
| `Payment_Due_Date` | string | no |  |
| `Discount_Due_Date` | string | no |  |
| `Discount_Amount` | number | no |  |
| `Status` | string | no |  |
| `Payment_Status` | string | no |  |
| `Bank_Account_Code` | string | no |  |
| `Check_Number` | string | no |  |
| `Check_Date` | string | no |  |
| `Card_Number` | string | no |  |
| `AP_GL_Account` | string | no |  |
| `Cost_Center` | string | no |  |
| `Remarks` | string | no |  |
| `APInvoiceDetails[]` | array | no |  |
| `Images[]` | array | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST vendor/invoice` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor-invoice-multi-line.md) for the provider-specific parameters and requirements.

