# Clockify: List Invoice Payments

Lists all invoice payments in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-invoice-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-invoice-payments?connectionId=$CONNECTION_ID&workspaceId=string&invoiceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "invoiceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-invoice-payments?${params}`, {
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
| `invoiceId` | string<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "author": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "note": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `author` | string |  |
| `date` | date |  |
| `id` | string |  |
| `note` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/invoices/:invoiceId/payments` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoice-payments.md) for the provider-specific parameters and requirements.

