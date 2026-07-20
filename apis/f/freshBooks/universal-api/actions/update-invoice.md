# FreshBooks: Update Invoice

Updates an existing invoice in FreshBooks for an account.

```
PUT https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreshBooks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "invoiceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "invoiceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | FreshBooks accounting account ID. |
| `invoiceId` | string | yes | FreshBooks invoice ID. |
| `invoice.customerid` | number | no |  |
| `invoice.create_date` | string | no |  |
| `invoice.due_date` | string | no |  |
| `invoice.notes` | string | no |  |
| `invoice.lines[].name` | string | no |  |
| `invoice.lines[].qty` | number | no |  |
| `invoice.lines[].unit_cost.amount` | string | no |  |
| `invoice.lines[].unit_cost.code` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountid": "string",
      "accountingSystemid": "string",
      "amount": {},
      "attachPdfToEmail": true,
      "autoBill": true,
      "autobillStatus": "string",
      "createdAt": "string",
      "createDate": "string",
      "currencyCode": "string",
      "currentOrganization": "string",
      "customerid": 1,
      "datePaid": "string",
      "depositStatus": "string",
      "description": "string",
      "discount": {},
      "discountDescription": "string",
      "discountTotal": {},
      "discountValue": "string",
      "displayStatus": "string",
      "dueDate": "string",
      "dueOffsetDays": 1,
      "estimateid": 1,
      "id": 1,
      "invoiceid": 1,
      "invoiceNumber": "string",
      "language": "string",
      "lockStatus": "string",
      "netPaidAmount": {},
      "notes": "string",
      "organization": "string",
      "outstanding": {},
      "ownerid": 1,
      "paid": {},
      "paymentDetails": "string",
      "paymentStatus": "string",
      "poNumber": "string",
      "senderAddress": {},
      "showAttachments": true,
      "status": 1,
      "template": "string",
      "terms": "string",
      "updated": "string",
      "uuid": "string",
      "v3Status": "string",
      "version": "string",
      "visState": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountid` | string |  |
| `accountingSystemid` | string |  |
| `amount` | object |  |
| `attachPdfToEmail` | boolean |  |
| `autoBill` | boolean |  |
| `autobillStatus` | string |  |
| `createdAt` | string |  |
| `createDate` | string |  |
| `currencyCode` | string |  |
| `currentOrganization` | string |  |
| `customerid` | number |  |
| `datePaid` | string |  |
| `depositStatus` | string |  |
| `description` | string |  |
| `discount` | object |  |
| `discountDescription` | string |  |
| `discountTotal` | object |  |
| `discountValue` | string |  |
| `displayStatus` | string |  |
| `dueDate` | string |  |
| `dueOffsetDays` | number |  |
| `estimateid` | number |  |
| `id` | number |  |
| `invoiceid` | number |  |
| `invoiceNumber` | string |  |
| `language` | string |  |
| `lockStatus` | string |  |
| `netPaidAmount` | object |  |
| `notes` | string |  |
| `organization` | string |  |
| `outstanding` | object |  |
| `ownerid` | number |  |
| `paid` | object |  |
| `paymentDetails` | string |  |
| `paymentStatus` | string |  |
| `poNumber` | string |  |
| `senderAddress` | object |  |
| `showAttachments` | boolean |  |
| `status` | number |  |
| `template` | string |  |
| `terms` | string |  |
| `updated` | string |  |
| `uuid` | string |  |
| `v3Status` | string |  |
| `version` | string |  |
| `visState` | number |  |

## Native endpoint

Through the native FreshBooks API, this operation is `PUT /accounting/account/:accountId/invoices/invoices/:invoiceId` (base URL `https://api.freshbooks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

