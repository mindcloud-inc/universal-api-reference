# Zoho Invoice: List Invoices

Retrieves invoices from Zoho Invoice.

```
GET https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-invoices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | list<string> | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `invoiceNumber` | string | no | An unique number given to the invoice. Maximum length [100] |
| `itemName` | string | no | item name. Variants: item_name_startswith and item_name_contains. Maximum length [100] |
| `itemId` | string | no | Unique item id. |
| `itemDescription` | string | no | Search invoices by item description. Variants: item_description_startswith and item_description_contains. Maximum length [100] |
| `referenceNumber` | string | no | The reference number of the invoice |
| `customerName` | string | no | The name of the customer. Maximum length [100] |
| `recurringInvoiceId` | string | no | ID of the recurring invoice from which the invoice is created. |
| `email` | string | no | Contact email ID. Maximum length [100] |
| `total` | string | no | The total amount to be paid |
| `balance` | string | no | The unpaid amount |
| `customField` | string | no | Custom fields for invoice. Variants: custom_field_startswith and custom_field_contains |
| `date` | date | no | Invoice date. Date format yyyy-mm-dd. Variants: due_date_start, due_date_end, due_date_before, due_date_after. |
| `dueDate` | date | no | Due date of the invoices. Date format yyyy-mm-dd. Variants: due_date_start, due_date_end, due_date_before, due_date_after. |
| `status` | list<string> | no | Search invoices by invoice status. Allowed values: sent, draft, overdue, paid, void, unpaid, partially_paid, viewed. One of: `draft`, `overdue`, `paid`, `partially_paid`, `sent`, `unpaid`, `viewed`, `void`. |
| `customerId` | string | no | ID of the customer to whom the invoice is created. |
| `filterBy` | list<string> | no | Filter invoices by any status or payment expected date. One of: `Date.PaymentExpectedDate`, `Status.All`, `Status.Draft`, `Status.OverDue`, `Status.Paid`, `Status.PartiallyPaid`, `Status.Sent`, `Status.Unpaid`, `Status.Viewed`, `Status.Void`. |
| `searchText` | string | no | Search invoices by invoice number, purchase order, or customer name. Maximum length [100] |
| `zcrmPotentialId` | number | no | Potential ID of a Deal in CRM. |

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

Through the native Zoho Invoice API, this operation is `GET /invoices` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

