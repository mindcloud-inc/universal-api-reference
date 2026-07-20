# Zoho Invoice: Update Invoice

Updates an invoice in Zoho Invoice.

```
PUT https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "invoiceId": "string",
  "customerId": "string",
  "lineItems[]": [
    {}
  ],
  "lineItems[].itemId": "string",
  "lineItems[].rate": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "invoiceId": "string",
    "customerId": "string",
    "lineItems[]": [{}],
    "lineItems[].itemId": "string",
    "lineItems[].rate": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | list<string> | yes | Unique identifier of the organization. |
| `adjustmentDescription` | string | no | Customize the adjustment description. |
| `avataxExemptNo` | string | no | Avalara exemption certificate number. |
| `avataxTaxCode` | string | no | Avalara tax code. |
| `avataxUseCode` | string | no | Avalara use code. |
| `cfdiUsage` | string | no | CFDI usage code for Mexico. |
| `customBody` | string | no | Customized email content for the invoice. |
| `customFields[].label` | string | no | Name of the custom field. |
| `customFields[].value` | string | no | Value of the custom field. |
| `customSubject` | string | no | Customized email subject for the invoice. |
| `gstNo` | string | no | GST number for the invoice. |
| `invoicedEstimateId` | string | no | ID of the estimate from which the invoice is created. |
| `invoiceId` | string | yes | Unique identifier of the invoice. |
| `invoiceNumber` | string | no | Unique invoice number. |
| `lineItems[].avataxExemptNo` | string | no | Avalara exemption certificate number for the line item. |
| `lineItems[].avataxUseCode` | string | no | Avalara use code for the line item. |
| `lineItems[].description` | string | no | Description of the line item. |
| `lineItems[].expenseId` | string | no | Expense ID associated with the line item. |
| `lineItems[].hsnOrSac` | string | no | HSN or SAC code. |
| `lineItems[].name` | string | no | Name of the line item. |
| `lineItems[].productType` | string | no | Product type of the line item. |
| `lineItems[].satItemKeyCode` | string | no | SAT item key code. |
| `lineItems[].taxExemptionId` | string | no | Tax exemption ID for the line item. |
| `lineItems[].taxId` | string | no | Tax ID applied to the line item. |
| `lineItems[].taxName` | string | no | Tax name for the line item. |
| `lineItems[].taxType` | string | no | Tax type for the line item. |
| `lineItems[].tdsTaxId` | string | no | TDS tax ID applied to the line item. |
| `lineItems[].unit` | string | no | Unit of the line item. |
| `lineItems[].unitkeyCode` | string | no | Unit key code. |
| `notes` | string | no | Notes added to the invoice. |
| `paymentOptions.paymentGateways[].additionalField1` | string | no | Provider-specific additional field for the payment gateway. |
| `paymentOptions.paymentGateways[].gatewayName` | string | no | Name of the payment gateway. |
| `paymentTermsLabel` | string | no | Override label for the payment terms. |
| `projectId` | string | no | Project ID associated with the invoice. |
| `reason` | string | no | Description of the attachment or reason field used by Zoho. |
| `recurringInvoiceId` | string | no | ID of the recurring invoice from which the invoice is created. |
| `referenceNumber` | string | no | Reference number for the invoice. |
| `salespersonName` | string | no | Name of the salesperson linked to the invoice. |
| `shippingCharge` | string | no | Shipping charges applied to the invoice. |
| `taxAuthorityId` | string | no | ID of the tax authority. |
| `taxExemptionId` | string | no | ID of the tax exemption. |
| `taxTreatment` | string | no | Tax treatment for the invoice. |
| `templateId` | string | no | ID of the PDF template associated with the invoice. |
| `terms` | string | no | Terms and conditions for the invoice. |
| `customerId` | string | yes | ID of the customer to whom the invoice is created. |
| `date` | date | no | Invoice date. |
| `lineItems[]` | array<object> | yes | Line items of the invoice. |
| `lineItems[].itemId` | string | yes | Unique item ID. |
| `lineItems[].rate` | number | yes | Rate of the line item. |
| `lineItems[].quantity` | number | no | Quantity of the line item. |
| `contactPersons[]` | array<string> | no | IDs of the contact persons associated with the contact. |
| `paymentTerms` | number | no | Payment terms in days. |
| `dueDate` | date | no | Due date for the invoice. |
| `discount` | number | no | Discount applied to the invoice. |
| `discountType` | list<string> | no | Type of discount applied to the invoice. One of: `options`. |
| `isDiscountBeforeTax` | boolean | no | Whether discount is applied before tax. |
| `isInclusiveTax` | boolean | no | Whether the tax is inclusive. |
| `exchangeRate` | number | no | Exchange rate of the currency. |
| `adjustment` | number | no | Adjustment made to the invoice. |
| `customFields[]` | array<object> | no | Custom fields for the invoice. |
| `lineItems[].projectId` | string | no | Project ID associated with the line item. |
| `lineItems[].timeEntryIds[]` | array<string> | no | Time entry IDs linked to the line item project. |
| `lineItems[].itemOrder` | number | no | Display order of the line item. |
| `lineItems[].discount` | number | no | Discount applied to the line item. |
| `lineItems[].taxPercentage` | number | no | Tax percentage for the line item. |
| `lineItems[].itemTotal` | number | no | Total amount of the line item. |
| `paymentOptions` | object | no | Payment options for the invoice. |
| `paymentOptions.paymentGateways[]` | array<object> | no | Payment gateways configured for the invoice. |
| `paymentOptions.paymentGateways[].configured` | boolean | no | Whether the payment gateway is configured. |
| `allowPartialPayments` | boolean | no | Whether partial payments are allowed for the invoice. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ignoreAutoNumberGeneration` | boolean | no | Ignore auto invoice number generation for this invoice. |
| `placeOfSupply` | string | no | Place of supply for GST/VAT. |
| `gstTreatment` | string | no | GST treatment for the invoice. |
| `vatTreatment` | string | no | VAT treatment for the invoice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "companyName": "Ava Chen",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "customerId": "string",
      "customerName": "Ava Chen",
      "date": "2026-05-07T12:00:00.000Z",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "invoiceId": "string",
      "invoiceNumber": "string",
      "invoiceUrl": "https://example.com",
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "referenceNumber": "string",
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `companyName` | string |  |
| `createdTime` | date |  |
| `currencyCode` | string |  |
| `customerId` | string |  |
| `customerName` | string |  |
| `date` | date |  |
| `dueDate` | date |  |
| `invoiceId` | string |  |
| `invoiceNumber` | string |  |
| `invoiceUrl` | string |  |
| `lastModifiedTime` | date |  |
| `referenceNumber` | string |  |
| `status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Zoho Invoice API, this operation is `PUT /invoices/:invoice_id` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

