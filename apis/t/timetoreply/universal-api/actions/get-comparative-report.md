# Timetoreply: Get Comparative Report



```
GET https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/get-comparative-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetoreply `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/get-comparative-report?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/get-comparative-report?${params}`, {
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
| `from` | string | no | Start date in YYYY-MM-DD format. |
| `model` | string | no | ID, name, email address, or domain to report on. |
| `modelType` | string | no | Model type for the selected model. |
| `search` | string | no | Search for a specific email subject line. |
| `to` | string | no | End date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentStats": {},
      "replyTimePercentages": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentStats` | object |  |
| `replyTimePercentages` | object |  |

## Native endpoint

Through the native Timetoreply API, this operation is `GET /api/reports/comparative` (base URL `https://portal.timetoreply.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-comparative-report.md) for the provider-specific parameters and requirements.

