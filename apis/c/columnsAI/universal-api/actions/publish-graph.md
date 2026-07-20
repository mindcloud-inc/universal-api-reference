# Columns AI: Publish Graph

Publishes a graph to Columns AI.

```
POST https://connect.mindcloud.co/v1/universal/columnsAI/latest/actions/publish-graph
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Columns AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/columnsAI/latest/actions/publish-graph" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "g-example",
  "name": "Quarterly Sales",
  "graph": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/columnsAI/latest/actions/publish-graph', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "g-example",
    "name": "Quarterly Sales",
    "graph": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Tracking ID included in the publish request body. Example: `g-example`. |
| `name` | string | yes | Name for the published Columns graph. Example: `Quarterly Sales`. |
| `graph` | object | yes | Columns GraphData object to publish. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Columns AI API returns.

## Native endpoint

Through the native Columns AI API, this operation is `POST /sdk/graph` (base URL `https://columns.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-graph.md) for the provider-specific parameters and requirements.

