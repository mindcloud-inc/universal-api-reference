# Merit: Create Purchase Invoice Waiting Approval



```
POST https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-purchase-invoice-waiting-approval
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-purchase-invoice-waiting-approval" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vendor": {},
  "docDate": "20260422",
  "dueDate": "20260429",
  "billNo": "MC-PO-20260422-2",
  "invoiceRow[]": [
    {}
  ],
  "taxAmount[]": [
    {}
  ],
  "totalAmount": 1,
  "totalSum": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-purchase-invoice-waiting-approval', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vendor": {},
    "docDate": "20260422",
    "dueDate": "20260429",
    "billNo": "MC-PO-20260422-2",
    "invoiceRow[]": [{}],
    "taxAmount[]": [{}],
    "totalAmount": 1,
    "totalSum": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vendor` | object | yes | Vendor object. |
| `docDate` | string | yes | Document date in YYYYmmDD format. Example: `20260422`. |
| `dueDate` | string | yes | Due date in YYYYmmDD format. Example: `20260429`. |
| `billNo` | string | yes | Bill number. Example: `MC-PO-20260422-2`. |
| `expenseClaim` | boolean | no | Whether this purchase order is an expense claim. |
| `currencyCode` | string | no | Currency code. Example: `EUR`. |
| `invoiceRow[]` | array<object> | yes | Array of purchase order row objects. |
| `taxAmount[]` | array<object> | yes | Array of VAT amount objects. |
| `totalAmount` | number | yes | Amount without VAT. |
| `totalSum` | number | yes | Amount with VAT. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Merit API returns.

## Native endpoint

Through the native Merit API, this operation is `POST v2/sendpurchorder` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase-invoice-waiting-approval.md) for the provider-specific parameters and requirements.

