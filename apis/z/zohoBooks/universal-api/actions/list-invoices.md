# Zoho Books: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-invoices?${params}`, {
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
| `customerId` | string | no | Search invoices by customer ID. |
| `invoiceNumber` | string | no | Search invoices by invoice number. |
| `status` | list | no | Search invoices by invoice status. One of: `draft`, `overdue`, `paid`, `partially_paid`, `sent`, `unpaid`, `viewed`, `void`. |
| `date` | date | no | Search invoices by invoice date in yyyy-mm-dd format. |
| `dueDate` | date | no | Search invoices by due date in yyyy-mm-dd format. |
| `searchText` | string | no | Search invoices by invoice number, purchase order, or customer name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemId` | string | no | Search invoices by item ID. |
| `sortColumn` | list | no | Sort invoices by a supported column. One of: `balance`, `created_time`, `customer_name`, `date`, `due_date`, `invoice_number`, `total`. |

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
      "currencySymbol": "string",
      "currentSubStatus": "string",
      "customerId": "string",
      "customerName": "Ava Chen",
      "date": "2026-05-07T12:00:00.000Z",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "hasAttachment": true,
      "invoiceId": "string",
      "invoiceNumber": "string",
      "isEmailed": true,
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "tags": [
        {}
      ],
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
| `currencySymbol` | string |  |
| `currentSubStatus` | string |  |
| `customerId` | string |  |
| `customerName` | string |  |
| `date` | date |  |
| `dueDate` | date |  |
| `hasAttachment` | boolean |  |
| `invoiceId` | string |  |
| `invoiceNumber` | string |  |
| `isEmailed` | boolean |  |
| `lastModifiedTime` | date |  |
| `status` | string |  |
| `tags` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Zoho Books API, this operation is `GET /invoices` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

