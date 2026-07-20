# FreshBooks: List Invoices

Retrieves invoices from FreshBooks for an account.

```
GET https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreshBooks `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/list-invoices?${params}`, {
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
| `accountId` | string | yes | FreshBooks accounting account ID. |

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

Through the native FreshBooks API, this operation is `GET /accounting/account/:accountId/invoices/invoices` (base URL `https://api.freshbooks.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

