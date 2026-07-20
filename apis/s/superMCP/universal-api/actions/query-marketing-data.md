# SuperMCP: Query Marketing Data



```
GET https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/query-marketing-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperMCP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/query-marketing-data?connectionId=$CONNECTION_ID&dataSourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataSourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/query-marketing-data?${params}`, {
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
| `dataSourceId` | string | yes | Supermetrics data source ID to query. |
| `dataSourceAccounts[]` | array<string> | no | Account IDs from Discover Accounts. |
| `fields[]` | array<string> | no | Metric and dimension field IDs to query. |
| `dateRangeType` | string | no | Use custom with start and end dates, or a documented relative range such as last_7_days. |
| `startDate` | date | no | Start date in YYYY-MM-DD format when date range type is custom. |
| `endDate` | date | no | End date in YYYY-MM-DD format when date range type is custom. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timezone` | string | no | Optional IANA timezone for date calculations. |
| `filters` | string | no | Optional Supermetrics filter expression. |
| `maxRows` | number | no | Maximum rows to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "schedule_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `schedule_id` | string | Opaque schedule ID for retrieving async query results. |

## Native endpoint

Through the native SuperMCP API, this operation is `POST /mcp/data_query` (base URL `https://mcp.supermetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-marketing-data.md) for the provider-specific parameters and requirements.

