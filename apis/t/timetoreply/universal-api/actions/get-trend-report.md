# Timetoreply: Get Trend Report



```
GET https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/get-trend-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetoreply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/get-trend-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/get-trend-report?${params}`, {
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
| `date` | string | no | Starting date for the trend report. |
| `model` | string | no | ID, name, email address, or domain to report on. |
| `modelType` | string | no | Model type for the selected model. |
| `periods` | number | no | Number of periods to include. |
| `periodType` | string | no | Period unit for the trend report. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dates": [
        "string"
      ],
      "page": 1,
      "stats": {},
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dates` | array |  |
| `page` | number |  |
| `stats` | object |  |
| `total` | number |  |

## Native endpoint

Through the native Timetoreply API, this operation is `GET /api/reports/trend` (base URL `https://portal.timetoreply.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trend-report.md) for the provider-specific parameters and requirements.

