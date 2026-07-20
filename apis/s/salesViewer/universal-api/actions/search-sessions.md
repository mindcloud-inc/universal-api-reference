# SalesViewer: Search Sessions

Finds sessions in SalesViewer by query parameters.

```
GET https://connect.mindcloud.co/v1/universal/salesViewer/latest/actions/search-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesViewer `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesViewer/latest/actions/search-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesViewer/latest/actions/search-sessions?${params}`, {
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
| `from` | string | no | Starting datetime for the session query. |
| `include_company` | boolean | no | Include company details in each session. |
| `include_company_sector` | boolean | no | Include company sector when company data is requested. |
| `include_hidden` | boolean | no | Include frontend-hidden companies. |
| `include_visits` | boolean | no | Include visit details in each session. |
| `locale` | string | no | Locale used for localized output fields. |
| `page` | number | no | 1-based result page number. |
| `page_size` | number | no | Number of entries per page. |
| `query` | string | no | SVQL query string used to filter sessions. |
| `timezone` | string | no | Timezone used for input and output datetimes. |
| `to` | string | no | Ending datetime for the session query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "current": 1,
        "isFirst": true,
        "isLast": true,
        "pageSize": 1,
        "total": 1,
        "totalItems": 1
      },
      "result": [
        {}
      ],
      "totals": {
        "companies": 1,
        "interest_visits": 1,
        "interests": 1,
        "sessions": 1,
        "visits": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.current` | number | Current 1-based page number. |
| `pagination.isFirst` | boolean | Whether the current page is the first page. |
| `pagination.isLast` | boolean | Whether the current page is the last page. |
| `pagination.pageSize` | number | Number of entries per page. |
| `pagination.total` | number | Total number of available records reported by SalesViewer. |
| `pagination.totalItems` | number | Total number of items available across all pages. |
| `result` | array<object> | List of session records returned by SalesViewer. |
| `totals.companies` | number | Total number of unique companies in the result set. |
| `totals.interest_visits` | number | Total number of interest-triggering visits in the result set. |
| `totals.interests` | number | Total number of interests in the result set. |
| `totals.sessions` | number | Total number of unique sessions in the result set. |
| `totals.visits` | number | Total number of page visits in the result set. |

## Native endpoint

Through the native SalesViewer API, this operation is `GET /sessions.json` (base URL `https://api.salesviewer.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-sessions.md) for the provider-specific parameters and requirements.

