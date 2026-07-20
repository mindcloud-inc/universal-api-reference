# Tidely: Create Invoice



```
POST https://connect.mindcloud.co/v1/universal/tidely/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tidely/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tidely/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactName` | string | no | Invoice contact name. |
| `dueDate` | string | no | Due date in YYYY-MM-DD format. |
| `invoiceDate` | string | no | Invoice date in YYYY-MM-DD format. |
| `invoiceId` | string | no | External invoice identifier. |
| `invoiceNumber` | string | no | Invoice number. |
| `invoiceStatus` | string | no | Tidely invoice status. |
| `invoiceType` | string | no | Tidely invoice type. |
| `openAmount` | string | no | Remaining open amount. |
| `totalGrossAmount` | string | no | Gross invoice amount. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoiceId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoiceId` | string | Tidely invoice identifier. |
| `success` | boolean | Whether the invoice operation succeeded. |

## Native endpoint

Through the native Tidely API, this operation is `POST /api/v1/open-api/invoices` (base URL `https://api.tidely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

