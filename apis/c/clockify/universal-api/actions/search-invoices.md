# Clockify: Search Invoices

Finds invoices in Clockify by filters.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/search-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/search-invoices?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/search-invoices?${params}`, {
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
| `workspaceId` | list<string> | yes |  |
| `clients` | object | no |  |
| `companies` | object | no |  |
| `exactAmount` | number | no | Example: `100`. |
| `exactBalance` | number | no | Example: `100`. |
| `greaterThanAmount` | number | no | Example: `100`. |
| `greaterThanBalance` | number | no | Example: `100`. |
| `invoiceNumber` | string | no |  |
| `issueDate` | object | no |  |
| `lessThanAmount` | number | no | Example: `100`. |
| `lessThanBalance` | number | no | Example: `100`. |
| `page` | number | no | Example: `100`. |
| `pageSize` | number | no | Example: `100`. |
| `sortColumn` | list<string> | no | One of: `AMOUNT`, `BALANCE`, `CLIENT`, `DUE_ON`, `ID`, `ISSUE_DATE`. |
| `sortOrder` | list<string> | no | One of: `ASCENDING`, `DESCENDING`. |
| `statuses[]` | array<string> | no |  |
| `strictSearch` | boolean | no | Example: `true`. |
| `clients.contains` | string | no |  |
| `clients.ids[]` | array<string> | no |  |
| `clients.status` | string | no |  |
| `companies.contains` | string | no |  |
| `companies.ids[]` | array<string> | no |  |
| `issueDate.issueDateEnd` | string | no |  |
| `issueDate.issueDateStart` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoices": [
        [
          {}
        ]
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
| `invoices[]` | array<object> |  |
| `invoices[].amount` | number |  |
| `invoices[].balance` | number |  |
| `invoices[].billFrom` | string |  |
| `invoices[].clientId` | string |  |
| `invoices[].clientName` | string |  |
| `invoices[].currency` | string |  |
| `invoices[].daysOverdue` | number |  |
| `invoices[].dueDate` | date |  |
| `invoices[].id` | string |  |
| `invoices[].issuedDate` | date |  |
| `invoices[].number` | string |  |
| `invoices[].paid` | number |  |
| `invoices[].status` | string |  |
| `invoices[].visibleZeroFields` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/invoices/info` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-invoices.md) for the provider-specific parameters and requirements.

