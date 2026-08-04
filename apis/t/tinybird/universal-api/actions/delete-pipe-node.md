# Tinybird: Delete Pipe Node



```
DELETE https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/delete-pipe-node
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinybird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/delete-pipe-node?connectionId=$CONNECTION_ID&name=Ava%20Chen&node=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "node": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/delete-pipe-node?${params}`, {
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
| `name` | string | yes | The pipe name to target. |
| `node` | string | yes | The pipe node name to target. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Tinybird API returns.

## Native endpoint

Through the native Tinybird API, this operation is `DELETE v0/pipes/:name/nodes/:node` (base URL `{{credentials.apiHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-pipe-node.md) for the provider-specific parameters and requirements.

