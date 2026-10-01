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
| `APInvoices[].APInvoiceDetails[].Amount` | number | no |  |
| `APInvoices[].APInvoiceDetails[].Distribution.Cost_Center` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Distribution.GL_Account` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Equipment.Equipment_Category` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Equipment.Equipment_Code` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Item_Description` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Job` | object | no |  |
| `APInvoices[].APInvoiceDetails[].Job.Cost_Type` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Job.Phase_Code` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Quantity` | number | no |  |
| `APInvoices[].APInvoiceDetails[].Tax_Code` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Unit_Of_Measure` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Work_Order.Component` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Work_Order.Equipment` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Work_Order.Service_Contract` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Work_Order.Unit_Price` | number | no |  |
| `APInvoices[].Images[].Document_ID` | string | no |  |
| `APInvoices[].Images[].Image_Description` | string | no |  |
| `APInvoices[].Images[].Image_File` | string | no | Base64 |
| `APInvoices[]` | array | no |  |
| `APInvoices[].APInvoiceDetails[].Distribution` | object | no |  |
| `APInvoices[].APInvoiceDetails[].Distribution.Company_Code` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Equipment.Equipment_Work_Order` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Job.Job_Number` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Work_Order.WO_Number` | string | no |  |
| `APInvoices[].Images[].Image_Type` | string | no |  |
| `APInvoices[].Invoice_Number` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Item_Code` | string | no |  |
| `APInvoices[].Vendor_Code` | string | no |  |
| `APInvoices[].Approval_Status` | string | no |  |
| `APInvoices[].Invoice_Type_Code` | string | no | I — Invoice [default] C — Credit memo |
| `APInvoices[].Routing_Code` | string | no |  |
| `APInvoices[].GL_Date` | string | no | Eg: 05/15/2017 |
| `APInvoices[].Invoice_Date` | string | no |  |
| `APInvoices[].Invoice_Amount` | number | no |  |
| `APInvoices[].APInvoiceDetails[].Equipment` | object | no |  |
| `APInvoices[].Sales_Tax_Amount` | number | no |  |
| `APInvoices[].APInvoiceDetails[].Work_Order` | object | no |  |
| `APInvoices[].VAT_Code` | string | no |  |
| `APInvoices[].APInvoiceDetails[].Remark` | string | no |  |
| `APInvoices[].Total_VAT_Amount` | string | no |  |
| `APInvoices[].Contract_Number` | string | no |  |
| `APInvoices[].Retention_Amount` | number | no |  |
| `APInvoices[].Batch_Code` | string | no |  |
| `APInvoices[].Payment_Due_Date` | string | no |  |
| `APInvoices[].Discount_Due_Date` | string | no |  |
| `APInvoices[].Discount_Amount` | number | no |  |
| `APInvoices[].Status` | string | no |  |
| `APInvoices[].Payment_Status` | string | no |  |
| `APInvoices[].Bank_Account_Code` | string | no |  |
| `APInvoices[].Check_Number` | string | no |  |
| `APInvoices[].Check_Date` | string | no |  |
| `APInvoices[].Card_Number` | string | no |  |
| `APInvoices[].AP_GL_Account` | string | no |  |
| `APInvoices[].Cost_Center` | string | no |  |
| `APInvoices[].Remarks` | string | no |  |
| `APInvoices[].APInvoiceDetails[]` | array | no |  |
| `APInvoices[].Images[]` | array | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST vendor/invoice` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor-invoice-multi-line.md) for the provider-specific parameters and requirements.

