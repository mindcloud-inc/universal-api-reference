# QuickBooks Online: Create Bill (Expense Lines)



```
POST https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-bill-expense-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-bill-expense-lines" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Line[].AccountBasedExpenseLineDetail.AccountRef": {},
  "Line[].AccountBasedExpenseLineDetail.AccountRef.value": "string",
  "Line[].Amount": 1,
  "VendorRef": {},
  "VendorRef.value": "string",
  "Line[]": [
    {}
  ],
  "Line[].AccountBasedExpenseLineDetail": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-bill-expense-lines', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Line[].AccountBasedExpenseLineDetail.AccountRef": {},
    "Line[].AccountBasedExpenseLineDetail.AccountRef.value": "string",
    "Line[].Amount": 1,
    "VendorRef": {},
    "VendorRef.value": "string",
    "Line[]": [{}],
    "Line[].AccountBasedExpenseLineDetail": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Line[].AccountBasedExpenseLineDetail.AccountRef` | object | yes |  |
| `Line[].AccountBasedExpenseLineDetail.AccountRef.value` | string | yes |  |
| `Line[].Amount` | number | yes |  |
| `VendorRef` | object | yes |  |
| `VendorRef.value` | string | yes |  |
| `Line[]` | array<object> | yes |  |
| `DocNumber` | string | no | Reference number for the transaction (shown as "Ref no." in QuickBooks). Maximum 21 characters. Must be unique unless the company allows duplicates. |
| `Line[].AccountBasedExpenseLineDetail` | object | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `CurrencyRef.value` | string | no |  |
| `Line[].AccountBasedExpenseLineDetail.AccountRef.name` | string | no |  |
| `Line[].Description` | string | no |  |
| `TxnDate` | string | no | Date in yyyy-mm-dd format. Example: `yyyy-mm-dd`. |
| `DueDate` | string | no | Date in yyyy-mm-dd format. Example: `yyyy-mm-dd`. |
| `PrivateNote` | string | no |  |
| `CurrencyRef` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native QuickBooks Online API returns.

## Native endpoint

Through the native QuickBooks Online API, this operation is `POST /bill` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bill-expense-lines.md) for the provider-specific parameters and requirements.

