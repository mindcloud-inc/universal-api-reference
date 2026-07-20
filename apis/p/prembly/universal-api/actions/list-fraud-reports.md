# Prembly: List Fraud Reports

Retrieves fraud reports from Prembly.

```
GET https://connect.mindcloud.co/v1/universal/prembly/latest/actions/list-fraud-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/list-fraud-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prembly/latest/actions/list-fraud-reports?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "filters": {
        "category": "string",
        "search": "string",
        "status": "string"
      },
      "pagination": {
        "has_next": true,
        "has_previous": true,
        "page": 1,
        "page_size": 1,
        "total_pages": 1,
        "total_records": 1
      },
      "reports": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "date_of_fraud": "2026-05-07T12:00:00.000Z",
          "fraud_category": "string",
          "fraud_type": "string",
          "full_name": "Ava Chen",
          "id": "string",
          "report_id": "string",
          "status": "string",
          "status_display": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filters.category` | string |  |
| `filters.search` | string |  |
| `filters.status` | string |  |
| `pagination.has_next` | boolean |  |
| `pagination.has_previous` | boolean |  |
| `pagination.page` | number |  |
| `pagination.page_size` | number |  |
| `pagination.total_pages` | number |  |
| `pagination.total_records` | number |  |
| `reports[].created_at` | date |  |
| `reports[].date_of_fraud` | date |  |
| `reports[].fraud_category` | string |  |
| `reports[].fraud_type` | string |  |
| `reports[].full_name` | string |  |
| `reports[].id` | string |  |
| `reports[].report_id` | string |  |
| `reports[].status` | string |  |
| `reports[].status_display` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `GET /api/v1/fraud/reports/` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fraud-reports.md) for the provider-specific parameters and requirements.

