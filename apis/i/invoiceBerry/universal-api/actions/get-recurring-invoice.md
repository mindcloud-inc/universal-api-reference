# InvoiceBerry: Get Recurring Invoice



```
GET https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-recurring-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InvoiceBerry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-recurring-invoice?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-recurring-invoice?${params}`, {
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
| `apiKey` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_send": "string",
      "client_firstname": "Ava",
      "client_id": "string",
      "client_lastname": "Chen",
      "client_name": "Ava Chen",
      "currency": "string",
      "discount": "string",
      "email_message": "ava@example.com",
      "email_own": "ava@example.com",
      "end_date": "2026-05-07T12:00:00.000Z",
      "frequency": "string",
      "id": "string",
      "items": [
        {}
      ],
      "language": "string",
      "last_invoice_date": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "payment_terms_days": "string",
      "po_number": "string",
      "profile_number": "string",
      "send_to": {},
      "start_date": "2026-05-07T12:00:00.000Z",
      "terms": "string",
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_send` | string |  |
| `client_firstname` | string |  |
| `client_id` | string |  |
| `client_lastname` | string |  |
| `client_name` | string |  |
| `currency` | string |  |
| `discount` | string |  |
| `email_message` | string |  |
| `email_own` | string |  |
| `end_date` | date |  |
| `frequency` | string |  |
| `id` | string |  |
| `items` | array<object> |  |
| `language` | string |  |
| `last_invoice_date` | date |  |
| `notes` | string |  |
| `payment_terms_days` | string |  |
| `po_number` | string |  |
| `profile_number` | string |  |
| `send_to` | object |  |
| `start_date` | date |  |
| `terms` | string |  |
| `total` | string |  |

## Native endpoint

Through the native InvoiceBerry API, this operation is `POST /api` (base URL `https://www.invoiceberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recurring-invoice.md) for the provider-specific parameters and requirements.

