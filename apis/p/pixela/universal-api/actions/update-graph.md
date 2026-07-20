# Pixela: Update Graph

Updates an existing graph definition in Pixela.

```
PUT https://connect.mindcloud.co/v1/universal/pixela/latest/actions/update-graph
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pixela `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pixela/latest/actions/update-graph" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "Ava Chen",
  "graph_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixela/latest/actions/update-graph', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "Ava Chen",
    "graph_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | yes | Pixela username in the request path. |
| `graph_id` | string | yes | Pixela graph identifier. |
| `name` | string | no | Updated graph display name. |
| `unit` | string | no | Updated unit for recorded quantities. |
| `color` | string | no | Updated graph color: shibafu, momiji, sora, ichou, ajisai, or kuro. |
| `timezone` | string | no | TZ database timezone name, such as UTC or Asia/Tokyo. |
| `description` | string | no | Graph description, up to 256 characters. |
| `startOnMonday` | boolean | no | Make the calendar heatmap start on Monday. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `purgeCacheURLs[]` | array<string> | no | Advanced list of URLs to purge when the graph is updated. Maximum 5 URLs. |
| `selfSufficient` | string | no | Supporter-limited SVG self-recording mode: none, increment, or decrement. |
| `isSecret` | boolean | no | Supporter-limited option to hide this graph from the graph list page. |
| `publishOptionalData` | boolean | no | Supporter-limited option to include optional pixel data in generated SVG attributes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isSuccess": true,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isSuccess` | boolean |  |
| `message` | string |  |

## Native endpoint

Through the native Pixela API, this operation is `PUT /v1/users/:username/graphs/:graphID` (base URL `https://pixe.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-graph.md) for the provider-specific parameters and requirements.

