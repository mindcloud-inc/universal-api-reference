# Zoho Books: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-contacts?${params}`, {
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
| `contactType` | list | no | Search contacts by contact type. Allowed values: customer or vendor. One of: `customer`, `vendor`. |
| `contactName` | string | no | Search contacts by contact name. |
| `email` | string | no | Search contacts by primary contact email. |
| `searchText` | string | no | Search contacts by contact name or notes. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterBy` | list | no | Filter contacts by documented contact or invoice status values. One of: `Invoice.OverDue`, `Invoice.Unpaid`, `Status.Active`, `Status.All`, `Status.CreditLimitExceed`, `Status.Crm`, `Status.Duplicate`, `Status.Inactive`, `Status.PortalDisabled`, `Status.PortalEnabled`. |
| `sortColumn` | list | no | Sort contacts by a supported column. One of: `contact_name`, `created_time`, `email`, `first_name`, `last_modified_time`, `last_name`, `outstanding_receivable_amount`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "achSupported": true,
      "companyName": "Ava Chen",
      "contactId": "string",
      "contactName": "Ava Chen",
      "contactType": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "customerName": "Ava Chen",
      "customerSubType": "string",
      "email": "ava@example.com",
      "hasAttachment": true,
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "outstandingPayableAmount": 1,
      "outstandingReceivableAmount": 1,
      "status": "string",
      "tags": [
        {}
      ],
      "vendorName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `achSupported` | boolean |  |
| `companyName` | string |  |
| `contactId` | string |  |
| `contactName` | string |  |
| `contactType` | string |  |
| `createdTime` | date |  |
| `currencyCode` | string |  |
| `customerName` | string |  |
| `customerSubType` | string |  |
| `email` | string |  |
| `hasAttachment` | boolean |  |
| `lastModifiedTime` | date |  |
| `outstandingPayableAmount` | number |  |
| `outstandingReceivableAmount` | number |  |
| `status` | string |  |
| `tags` | array<object> |  |
| `vendorName` | string |  |

## Native endpoint

Through the native Zoho Books API, this operation is `GET /contacts` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

