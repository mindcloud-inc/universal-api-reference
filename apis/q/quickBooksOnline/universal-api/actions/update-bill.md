# QuickBooks Online: Update Bill



```
PUT https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/update-bill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/update-bill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Id": "string",
  "Line[].AccountBasedExpenseLineDetail.AccountRef": {},
  "Line[].AccountBasedExpenseLineDetail.AccountRef.value": "string",
  "VendorRef.value": "string",
  "Line[].Amount": 1,
  "SyncToken": "string",
  "VendorRef": {},
  "Line[].AccountBasedExpenseLineDetail": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/update-bill', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Id": "string",
    "Line[].AccountBasedExpenseLineDetail.AccountRef": {},
    "Line[].AccountBasedExpenseLineDetail.AccountRef.value": "string",
    "VendorRef.value": "string",
    "Line[].Amount": 1,
    "SyncToken": "string",
    "VendorRef": {},
    "Line[].AccountBasedExpenseLineDetail": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Id` | string | yes | ID of the existing bill to update. |
| `Line[].AccountBasedExpenseLineDetail.AccountRef` | object | yes |  |
| `Line[].AccountBasedExpenseLineDetail.AccountRef.value` | string | yes |  |
| `Line[].Id` | string | no | Existing line ID. Include it to keep or modify this line when replacing the bill's lines. |
| `VendorRef.value` | string | yes |  |
| `Line[].Amount` | number | yes |  |
| `SyncToken` | string | yes | Current SyncToken from the bill's latest data, such as a Get Bill or Create Bill result. It changes every time the bill is saved. QuickBooks rejects updates with a stale SyncToken. |
| `VendorRef` | object | yes |  |
| `Line[]` | array<object> | no | Sending Line replaces all of the bill's lines; lines not sent are deleted. Include every line you want to keep, and include its existing line Id to keep or modify that line. Omit Line to leave all lines unchanged. |
| `Line[].AccountBasedExpenseLineDetail` | object | yes |  |
| `DocNumber` | string | no | Reference number for the transaction (shown as "Ref no." in QuickBooks). Maximum 21 characters. Must be unique unless the company allows duplicates. |

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

Through the native QuickBooks Online API, this operation is `POST /bill` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bill.md) for the provider-specific parameters and requirements.

