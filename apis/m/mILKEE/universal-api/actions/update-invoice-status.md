# MILKEE: Update Invoice Status

Updates an invoice status in MILKEE.

```
PUT https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/update-invoice-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MILKEE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/update-invoice-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "4640",
  "invoiceId": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/update-invoice-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "4640",
    "invoiceId": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bankAccountId` | number | no | Bank account ID for payment booking. |
| `companyId` | string | yes | The numeric MILKEE company ID used in the request path. Default: `4640`. |
| `createEntry` | boolean | no | Create an accounting entry when marking the invoice as paid. |
| `invoiceId` | string | yes | The numeric MILKEE invoice ID used in the request path. |
| `paidDate` | string | no | Payment date for the paid transition. |
| `status` | string | yes | Target invoice status transition. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native MILKEE API, this operation is `GET /companies/:companyId/invoices/:invoiceId/mark-as` (base URL `https://app.milkee.ch/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice-status.md) for the provider-specific parameters and requirements.

