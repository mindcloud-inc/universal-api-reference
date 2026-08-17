# Zenoti: Get Sales Report



```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-sales?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-sales?${params}`, {
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
| `centres[].centre` | list | no |  |
| `invoiceStatuses[].invoiceStatus` | list | no |  |
| `itemTypes[].itemType` | list | no |  |
| `paymentTypes[].paymentType` | list | no |  |
| `saleTypes[].salesType` | list | no |  |
| `startDate` | date | no |  |
| `endDate` | date | no |  |
| `centres[]` | array | no |  |
| `soldBy[]` | array<string> | no | Employee IDs |
| `itemTypes[]` | array | no |  |
| `paymentTypes[]` | array | no |  |
| `saleTypes[]` | array<object> | no |  |
| `invoiceStatuses[]` | array<object> | no |  |
| `includeTotal` | boolean | no | Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zenoti API returns.

## Native endpoint

Through the native Zenoti API, this operation is `POST reports/sales/accrual_basis/flat_file` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sales.md) for the provider-specific parameters and requirements.

