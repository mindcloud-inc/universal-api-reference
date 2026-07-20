# QuickBooks Online: Get Profit and Loss



```
GET https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/get-profit-and-loss
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/get-profit-and-loss?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/get-profit-and-loss?${params}`, {
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
| `start_date` | string | no | Start date for the report period. Use YYYY-MM-DD format. Example: `2026-01-01`. |
| `end_date` | string | no | End date for the report period. Use YYYY-MM-DD format. Example: `2026-03-31`. |
| `accounting_method` | list | no | Accounting basis to use for the report, such as Cash or Accrual. One of: `0`, `1`. |
| `summarize_column_by` | list | no | Column grouping for the report, such as Total, Month, or Customers. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | string | no | Optional QuickBooks customer ID filter. |
| `vendor` | string | no | Optional QuickBooks vendor ID filter. |
| `class` | string | no | Optional QuickBooks class ID filter. |
| `department` | string | no | Optional QuickBooks department ID filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Columns": {},
      "Header": {},
      "Rows": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Columns` | object | Report column definitions returned by QuickBooks. |
| `Header` | object | Report metadata including report name, basis, period, currency, and options. |
| `Rows` | object | Nested report rows, sections, summaries, and data rows returned by QuickBooks. |

## Native endpoint

Through the native QuickBooks Online API, this operation is `GET /reports/ProfitAndLoss` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profit-and-loss.md) for the provider-specific parameters and requirements.

