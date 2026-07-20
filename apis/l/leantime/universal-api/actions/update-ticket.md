# Leantime: Update Ticket



```
PUT https://connect.mindcloud.co/v1/universal/leantime/latest/actions/update-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/update-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.values.id": 1,
  "params.values.projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leantime/latest/actions/update-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.values.id": 1,
    "params.values.projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.values.id` | number | yes | The ticket ID to update. |
| `params.values.projectId` | number | yes | The project that owns the ticket. |
| `params.values.headline` | string | no | Updated ticket headline. |
| `params.values.description` | string | no | Updated ticket description. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.values.status` | number | no | Updated numeric status ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leantime API returns.

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ticket.md) for the provider-specific parameters and requirements.

