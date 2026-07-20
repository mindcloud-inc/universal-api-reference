# Invoiless: Update Invoice

Updates an existing invoice in Invoiless.

```
PUT https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoiless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Invoice id. |
| `customer` | string | no | Customer id. The Invoiless docs also allow an object here, but this draft currently standardizes on a customer id string. |
| `items[]` | array<object> | no | Invoice line items array. |
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

Through the native Invoiless API, this operation is `PUT /invoices/:id` (base URL `https://api.invoiless.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

