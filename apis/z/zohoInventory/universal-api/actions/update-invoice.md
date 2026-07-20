# Zoho Inventory: Update Invoice

Updates an existing invoice in Zoho Inventory.

```
PUT https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": "string",
  "organizationId": "{{credentials.organizationId}}",
  "customerId": "string",
  "lineItems[]": [
    {}
  ],
  "lineItems[].itemId": "string",
  "lineItems[].quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": "string",
    "organizationId": "{{credentials.organizationId}}",
    "customerId": "string",
    "lineItems[]": [{}],
    "lineItems[].itemId": "string",
    "lineItems[].quantity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | string | yes | The Zoho Inventory invoice_id for the invoice. |
| `organizationId` | string | yes | Zoho Inventory organization ID to run this request against. Default: `{{credentials.organizationId}}`. |
| `customerId` | string | yes | Customer to bill on the invoice. |
| `invoiceNumber` | string | no | Invoice number for this invoice. |
| `date` | string | no | Invoice date in YYYY-MM-DD format. |
| `dueDate` | string | no | Invoice due date in YYYY-MM-DD format. |
| `referenceNumber` | string | no | External reference number for the invoice. |
| `lineItems[]` | array<object> | yes | One or more invoice line items. |
| `lineItems[].lineItemId` | string | no | Existing line item identifier when updating a line. |
| `lineItems[].itemId` | string | yes | Item to set on this invoice line. |
| `lineItems[].quantity` | number | yes | Quantity to invoice for this line. |
| `lineItems[].rate` | number | no | Rate for this invoice line item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "created_time": "string",
      "customer_id": "string",
      "customer_name": "Ava Chen",
      "date": "string",
      "due_date": "string",
      "invoice_id": "string",
      "invoice_number": "string",
      "last_modified_time": "string",
      "line_items": [
        {}
      ],
      "notes": "string",
      "reference_number": "string",
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
| `created_time` | string |  |
| `customer_id` | string |  |
| `customer_name` | string |  |
| `date` | string |  |
| `due_date` | string |  |
| `invoice_id` | string |  |
| `invoice_number` | string |  |
| `last_modified_time` | string |  |
| `line_items` | array<object> |  |
| `notes` | string |  |
| `reference_number` | string |  |
| `status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Zoho Inventory API, this operation is `PUT /invoices/:invoice_id` (base URL `{{credentials.accessTokenRequest.api_domain}}/inventory/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

