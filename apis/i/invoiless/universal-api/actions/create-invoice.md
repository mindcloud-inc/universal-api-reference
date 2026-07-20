# Invoiless: Create Invoice

Creates a new invoice in Invoiless.

```
POST https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoiless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer": "string",
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer": "string",
    "items[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | string | yes | Customer id. The Invoiless docs also allow an object here, but this draft currently standardizes on a customer id string. |
| `items[]` | array<object> | yes | Invoice line items array. |
| `number` | string | no | Invoice number. |
| `date` | date | no | Invoice date. |
| `dueDate` | date | no | Invoice due date. |
| `currency` | string | no | ISO 4217 currency code. |
| `lang` | string | no | Invoice language code. |
| `status` | string | no | Invoice status. |
| `terms` | string | no | Invoice terms. |
| `notes` | string | no | Invoice notes. |
| `tags[]` | array<string> | no | Invoice tags. |
| `taxIncluded` | boolean | no | Whether tax is included in prices. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Invoiless API, this operation is `POST /invoices` (base URL `https://api.invoiless.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

