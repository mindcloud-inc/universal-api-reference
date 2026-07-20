# Better Stack Uptime: List Incidents

Retrieves incidents from Better Stack Uptime.

```
GET https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/list-incidents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Uptime `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/list-incidents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/list-incidents?${params}`, {
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
| `teamName` | string | no | Filter incidents for a specific Better Stack team when using a global API token. |
| `from` | string | no | Return incidents from this date (YYYY-MM-DD). |
| `to` | string | no | Return incidents until this date (YYYY-MM-DD). |
| `monitorId` | string | no | Filter incidents for a specific monitor. |
| `heartbeatId` | string | no | Filter incidents for a specific heartbeat. |
| `resolved` | boolean | no | Filter to resolved or unresolved incidents. |
| `acknowledged` | boolean | no | Filter to acknowledged or unacknowledged incidents. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Uptime API returns.

## Native endpoint

Through the native Better Stack Uptime API, this operation is `GET /v3/incidents` (base URL `https://uptime.betterstack.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-incidents.md) for the provider-specific parameters and requirements.

