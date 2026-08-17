# Zenoti: Get Sales Accrual Report



```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/get-sales-accrual-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/get-sales-accrual-report?connectionId=$CONNECTION_ID&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/get-sales-accrual-report?${params}`, {
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
| `center_ids[].center` | list | no |  |
| `invoiceStatuses[].invoiceStatus` | list | no |  |
| `itemTypes[].itemType` | list | no |  |
| `paymentTypes[].paymentType` | list | no |  |
| `saleTypes[].saleType` | list | no |  |
| `startDate` | date | yes |  |
| `endDate` | date | yes |  |
| `center_ids[]` | array | no |  |
| `itemTypes[]` | array | no |  |
| `paymentTypes[]` | array | no |  |
| `saleTypes[]` | array | no |  |
| `invoiceStatuses[]` | array | no |  |
| `includeTotal` | boolean | no | Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zenoti API returns.

## Native endpoint

Through the native Zenoti API, this operation is `POST reports/sales/accrual_basis/flat_file` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sales-accrual-report.md) for the provider-specific parameters and requirements.

