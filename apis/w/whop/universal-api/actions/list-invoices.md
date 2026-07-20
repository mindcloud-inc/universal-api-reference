# Whop: List Invoices

Retrieves invoices from Whop for a company.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-invoices?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-invoices?${params}`, {
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
| `companyId` | string | yes | The unique identifier of the company to list invoices for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentPlan": {
        "currency": "string",
        "formattedPrice": "string",
        "id": "string"
      },
      "dueDate": "2026-05-07T12:00:00.000Z",
      "emailAddress": "ava@example.com",
      "id": "string",
      "number": "string",
      "status": "string",
      "user": {
        "id": "string",
        "name": "Ava Chen",
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `currentPlan` | object |  |
| `currentPlan.currency` | string |  |
| `currentPlan.formattedPrice` | string |  |
| `currentPlan.id` | string |  |
| `dueDate` | date |  |
| `emailAddress` | string |  |
| `id` | string |  |
| `number` | string |  |
| `status` | string |  |
| `user` | object |  |
| `user.id` | string |  |
| `user.name` | string |  |
| `user.username` | string |  |

## Native endpoint

Through the native Whop API, this operation is `GET /api/v1/invoices` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

