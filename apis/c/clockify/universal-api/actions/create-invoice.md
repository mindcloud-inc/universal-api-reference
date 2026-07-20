# Clockify: Create Invoice

Creates a new invoice in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "clientId": "string",
  "currency": "USD",
  "dueDate": "2026-01-01T00:00:00Z",
  "issuedDate": "2026-01-01T00:00:00Z",
  "number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "clientId": "string",
    "currency": "USD",
    "dueDate": "2026-01-01T00:00:00Z",
    "issuedDate": "2026-01-01T00:00:00Z",
    "number": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `clientId` | list<string> | yes |  |
| `currency` | string | yes | Example: `USD`. |
| `dueDate` | date | yes | Example: `2026-01-01T00:00:00Z`. |
| `issuedDate` | date | yes | Example: `2026-01-01T00:00:00Z`. |
| `number` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billFrom": "string",
      "clientId": "string",
      "currency": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "issuedDate": "2026-05-07T12:00:00.000Z",
      "number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billFrom` | string |  |
| `clientId` | string |  |
| `currency` | string |  |
| `dueDate` | date |  |
| `id` | string |  |
| `issuedDate` | date |  |
| `number` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/invoices` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

