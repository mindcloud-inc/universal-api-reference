# Socket: List Alerts

Retrieves latest organization alerts from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-alerts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-alerts?${params}`, {
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
| `filters.alertAction` | list<string> | no |  |
| `filters.alertCategory` | list<string> | no |  |
| `filters.alertKEV` | boolean | no |  |
| `filters.alertPriority` | list<string> | no |  |
| `filters.alertSeverity` | list<string> | no |  |
| `filters.alertStatus` | string | no |  |
| `filters.alertType` | list<string> | no |  |
| `perPage` | number | no |  |
| `startAfterCursor` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Socket API returns.

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/alerts` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alerts.md) for the provider-specific parameters and requirements.

