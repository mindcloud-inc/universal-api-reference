# Leantime: Create Ticket



```
POST https://connect.mindcloud.co/v1/universal/leantime/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.values.headline": "string",
  "params.values.projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leantime/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.values.headline": "string",
    "params.values.projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.values.headline` | string | yes | The ticket headline. |
| `params.values.projectId` | number | yes | The project that will own the ticket. |
| `params.values.description` | string | no | Ticket description. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.values.type` | string | no | Ticket type such as task or milestone. Default: `task`. |
| `params.values.status` | number | no | Numeric status ID for the ticket. Default: `3`. |
| `params.values.milestoneid` | number | no | Associated milestone ID. |
| `params.values.sprint` | number | no | Associated sprint ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leantime API returns.

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

