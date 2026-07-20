# Zoho Books: List Bills



```
GET https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-bills
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-bills?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-bills?${params}`, {
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
| `billNumber` | string | no | Filter bills by bill number. |
| `date` | string | no | Filter bills by bill date. |
| `description` | string | no | Filter bills by description. |
| `filterBy` | string | no | Filter bills by Zoho status constants. |
| `itemId` | string | no | Filter bills by item ID. |
| `lastModifiedTime` | string | no | Filter bills by last modification time. |
| `organizationId` | string | yes | ID of the organization. |
| `purchaseorderId` | string | no | Filter bills by purchase order ID. |
| `recurringBillId` | string | no | Filter bills by recurring bill ID. |
| `referenceNumber` | string | no | Filter bills by reference number. |
| `searchText` | string | no | Search across bill fields. |
| `sortColumn` | string | no | Sort bills by the selected column. |
| `sortOrder` | string | no | Sort bills in ascending (A) or descending (D) order. |
| `status` | string | no | Filter bills by status. |
| `total` | number | no | Filter bills by total amount. |
| `vendorId` | string | no | Filter bills by vendor ID. |
| `vendorName` | string | no | Filter bills by vendor name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bills": [
        {
          "balance": 1,
          "billId": "string",
          "billNumber": "string",
          "createdTime": "2026-05-07T12:00:00.000Z",
          "currencyCode": "string",
          "currencyId": "string",
          "currentSubStatus": "string",
          "date": "2026-05-07T12:00:00.000Z",
          "dueDate": "2026-05-07T12:00:00.000Z",
          "exchangeRate": 1,
          "hasAttachment": true,
          "lastModifiedTime": "2026-05-07T12:00:00.000Z",
          "pricePrecision": 1,
          "referenceNumber": "string",
          "status": "string",
          "total": 1,
          "vendorId": "string",
          "vendorName": "Ava Chen"
        }
      ],
      "code": 1,
      "message": "string",
      "pageContext": {
        "appliedFilter": "string",
        "hasMorePage": true,
        "page": 1,
        "perPage": 1,
        "reportName": "Ava Chen",
        "sortColumn": "string",
        "sortOrder": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bills[].balance` | number |  |
| `bills[].billId` | string |  |
| `bills[].billNumber` | string |  |
| `bills[].createdTime` | date |  |
| `bills[].currencyCode` | string |  |
| `bills[].currencyId` | string |  |
| `bills[].currentSubStatus` | string |  |
| `bills[].date` | date |  |
| `bills[].dueDate` | date |  |
| `bills[].exchangeRate` | number |  |
| `bills[].hasAttachment` | boolean |  |
| `bills[].lastModifiedTime` | date |  |
| `bills[].pricePrecision` | number |  |
| `bills[].referenceNumber` | string |  |
| `bills[].status` | string |  |
| `bills[].total` | number |  |
| `bills[].vendorId` | string |  |
| `bills[].vendorName` | string |  |
| `code` | number |  |
| `message` | string |  |
| `pageContext.appliedFilter` | string |  |
| `pageContext.hasMorePage` | boolean |  |
| `pageContext.page` | number |  |
| `pageContext.perPage` | number |  |
| `pageContext.reportName` | string |  |
| `pageContext.sortColumn` | string |  |
| `pageContext.sortOrder` | string |  |

## Native endpoint

Through the native Zoho Books API, this operation is `GET /bills` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bills.md) for the provider-specific parameters and requirements.

