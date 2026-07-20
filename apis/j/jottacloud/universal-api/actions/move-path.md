# Jottacloud: Move Path



```
PUT https://connect.mindcloud.co/v1/universal/jottacloud/latest/actions/move-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jottacloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jottacloud/latest/actions/move-path" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from_path": "string",
  "to_path": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jottacloud/latest/actions/move-path', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from_path": "string",
    "to_path": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from_path` | string | yes | Source logical path to move. |
| `to_path` | string | yes | Destination logical path for the moved item. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jottacloud API returns.

## Native endpoint

Through the native Jottacloud API, this operation is `POST /files/v2/move` (base URL `https://api.jotta.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-path.md) for the provider-specific parameters and requirements.

