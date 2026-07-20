# Leantime: Upsert Time Entry



```
POST https://connect.mindcloud.co/v1/universal/leantime/latest/actions/upsert-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/upsert-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": 1,
  "kind": "GENERAL_BILLABLE",
  "hours": 1,
  "timestamp": "1774979835"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leantime/latest/actions/upsert-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": 1,
    "kind": "GENERAL_BILLABLE",
    "hours": 1,
    "timestamp": "1774979835"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | number | yes | The ticket to upsert time against. |
| `kind` | string | yes | The timesheet entry type. Default: `GENERAL_BILLABLE`. |
| `hours` | number | yes | The number of hours to set. |
| `timestamp` | number | yes | Unix timestamp for the work date. Default: `1774979835`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leantime API returns.

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-time-entry.md) for the provider-specific parameters and requirements.

