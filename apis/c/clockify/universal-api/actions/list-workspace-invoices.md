# Clockify: List Workspace Invoices

Lists all workspace invoices in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-invoices?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-invoices?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statuses` | list<string> | no | One of: `OVERDUE`, `PAID`, `PARTIALLY_PAID`, `SENT`, `UNSENT`, `VOID`. Example: `ACTIVE`. |

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
| `invoices[].clientId` | string |  |
| `invoices[].clientName` | string |  |
| `invoices[].currency` | string |  |
| `invoices[].dueDate` | date |  |
| `invoices[].id` | string |  |
| `invoices[].issuedDate` | date |  |
| `invoices[].number` | string |  |
| `invoices[].paid` | number |  |
| `invoices[].status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/invoices` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-invoices.md) for the provider-specific parameters and requirements.

