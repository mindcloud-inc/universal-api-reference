# Zoho Invoice: List Expenses

Retrieves expenses from Zoho Invoice.

```
GET https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-expenses?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=10234695" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "10234695"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-expenses?${params}`, {
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
| `organizationId` | list<string> | yes | ID of the organization header X-com-zoho-invoice-organizationid. Example: `10234695`. |
| `searchText` | string | no | Search expenses by account name, description, customer name, or vendor name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `referenceNumber` | string | no | Search expenses by reference number. |
| `date` | date | no | Search expenses by expense date. |
| `status` | string | no | Search expenses by expense status. One of: `0`, `1`, `2`, `3`, `4`. |
| `amount` | number | no | Search expenses by amount. |
| `accountName` | string | no | Search expenses by expense account name. |
| `customerName` | string | no | Search expenses by customer name. |
| `sortColumn` | string | no | Sort expenses. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `filterBy` | string | no | Filter expenses by expense status. One of: `0`, `1`, `2`, `3`, `4`, `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "accountName": "Ava Chen",
      "amount": 1,
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "expenseId": "string",
      "isBillable": true,
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
| `accountId` | string |  |
| `accountName` | string |  |
| `amount` | number |  |
| `createdTime` | date |  |
| `currencyCode` | string |  |
| `date` | date |  |
| `description` | string |  |
| `expenseId` | string |  |
| `isBillable` | boolean |  |
| `lastModifiedTime` | date |  |
| `referenceNumber` | string |  |
| `status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Zoho Invoice API, this operation is `GET /expenses` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-expenses.md) for the provider-specific parameters and requirements.

