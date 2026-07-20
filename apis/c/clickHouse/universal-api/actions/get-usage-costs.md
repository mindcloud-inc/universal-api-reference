# ClickHouse: Get Usage Costs



```
GET https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-usage-costs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickHouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-usage-costs?connectionId=$CONNECTION_ID&organizationId=string&fromDate=2026-04-15&toDate=2026-04-16" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string",
  "fromDate": "2026-04-15",
  "toDate": "2026-04-16"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-usage-costs?${params}`, {
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
| `organizationId` | string | yes | ID of the requested organization. |
| `fromDate` | string | yes | Start date for the report in YYYY-MM-DD format, e.g. 2024-12-19. Example: `2026-04-15`. |
| `toDate` | string | yes | End date, inclusive, in YYYY-MM-DD format. This date cannot be more than 30 days after from_date. Example: `2026-04-16`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "costs": [
        {}
      ],
      "grandTotalCHC": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `costs` | array<object> | Daily per-entity usage cost records. |
| `grandTotalCHC` | number | Grand total usage cost in ClickHouse Credits. |

## Native endpoint

Through the native ClickHouse API, this operation is `GET /v1/organizations/[:organizationId]/usageCost` (base URL `https://api.clickhouse.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage-costs.md) for the provider-specific parameters and requirements.

