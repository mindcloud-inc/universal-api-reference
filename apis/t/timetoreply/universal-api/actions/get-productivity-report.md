# Timetoreply: Get Productivity Report



```
GET https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/get-productivity-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetoreply `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/get-productivity-report?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/get-productivity-report?${params}`, {
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
| `date` | string | no | Reference date for the productivity report. |
| `model` | string | no | ID, name, email address, or domain to report on. |
| `modelType` | string | no | Model type for the selected model. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activity": {},
      "average_reply_times": {},
      "conversations": {},
      "email_volumes": {},
      "page": 1,
      "responsiveness": {},
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
| `activity` | object |  |
| `average_reply_times` | object |  |
| `conversations` | object |  |
| `email_volumes` | object |  |
| `page` | number |  |
| `responsiveness` | object |  |
| `stats` | object |  |
| `total` | number |  |

## Native endpoint

Through the native Timetoreply API, this operation is `GET /api/reports/productivity` (base URL `https://portal.timetoreply.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-productivity-report.md) for the provider-specific parameters and requirements.

