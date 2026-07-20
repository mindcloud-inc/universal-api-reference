# Statsig: List Audit Logs

Retrieves audit logs from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/list-audit-logs-get-console-v1-audit-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/list-audit-logs-get-console-v1-audit-logs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/list-audit-logs-get-console-v1-audit-logs?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no |  |
| `sortKey` | string | no |  |
| `sortOrder` | string | no |  |
| `latestID` | string | no |  |
| `tags` | string | no |  |
| `actionType` | string | no |  |
| `actionTypes` | string | no |  |
| `startDate` | string | no | Expected valid date in the form of YYYY-MM-DD. Defaults to 90 days before endDate. If both dates are omitted, the endpoint searches the last 90 days. |
| `endDate` | string | no | Expected valid date in the form of YYYY-MM-DD. Defaults to today. If both dates are omitted, the endpoint searches the last 90 days. |
| `limit` | number | no | Results per page |
| `page` | number | no | Page number |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `GET /console/v1/audit_logs` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-audit-logs-get-console-v1-audit-logs.md) for the provider-specific parameters and requirements.

