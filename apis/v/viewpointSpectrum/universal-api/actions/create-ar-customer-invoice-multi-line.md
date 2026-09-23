# Viewpoint Spectrum: Create AR Customer Invoice Multi-Line



```
PUT https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-ar-customer-invoice-multi-line
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-ar-customer-invoice-multi-line" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-ar-customer-invoice-multi-line', {
  method: 'PUT',
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
| `arInvoices[]` | array | no |  |
| `arInvoices[].multiLineArInvoice` | object | no |  |
| `arInvoices[].multiLineArInvoice.Company_Code` | string | no |  |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail` | object | no |  |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.Quantity` | number | no |  |
| `arInvoices[].multiLineArInvoice.GL_Date` | string | no |  |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.Detail_Description` | string | no |  |
| `arInvoices[].multiLineArInvoice.Batch_Code` | string | no |  |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.Unit_Of_Measure` | string | no |  |
| `arInvoices[].multiLineArInvoice.Customer_Code` | string | no |  |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.Line_Extension` | number | no |  |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.GL_Account` | string | no |  |
| `arInvoices[].multiLineArInvoice.Job Number` | string | no |  |
| `arInvoices[].multiLineArInvoice.Invoice_Or_Transaction` | string | no |  |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.Taxable_Flag` | string | no |  |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.Income_Cost_Center` | string | no |  |
| `arInvoices[].multiLineArInvoice.Transaction_Type` | string | no |  |
| `arInvoices[].multiLineArInvoice.Invoice Date` | string | no |  |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.Message` | string | no |  |
| `arInvoices[].multiLineArInvoice.Terms_Code` | string | no |  |
| `arInvoices[].multiLineArInvoice.Salesperson_Code` | string | no |  |
| `arInvoices[].multiLineArInvoice.Sales_Tax_Code` | string | no |  |
| `arInvoices[].multiLineArInvoice.Sale_Tax_Amount` | number | no |  |
| `arInvoices[].multiLineArInvoice.Retention_Percent` | number | no |  |
| `arInvoices[].multiLineArInvoice.Print_Job_Address_Flag` | string | no |  |
| `arInvoices[].multiLineArInvoice.Remarks` | string | no |  |
| `arInvoices[].multiLineArInvoice.Customer_PO` | string | no |  |
| `arInvoices[].multiLineArInvoice.Retention_Amount` | number | no |  |
| `arInvoices[].multiLineArInvoice.VAT_Code` | string | no |  |
| `arInvoices[].multiLineArInvoice.Total_Vat_Amount` | number | no |  |
| `arInvoices[].multiLineArInvoice.Asset_Cost_Center` | string | no |  |
| `arInvoices[].multiLineArInvoice.invoiceDetails[]` | array | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST customer/invoice` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ar-customer-invoice-multi-line.md) for the provider-specific parameters and requirements.

