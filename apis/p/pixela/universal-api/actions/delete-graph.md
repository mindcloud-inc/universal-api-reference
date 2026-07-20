# Pixela: Delete Graph

Deletes an existing graph definition from Pixela.

```
DELETE https://connect.mindcloud.co/v1/universal/pixela/latest/actions/delete-graph
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pixela `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pixela/latest/actions/delete-graph?connectionId=$CONNECTION_ID&username=Ava%20Chen&graph_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen",
  "graph_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixela/latest/actions/delete-graph?${params}`, {
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
| `username` | string | yes | Pixela username in the request path. |
| `graph_id` | string | yes | Pixela graph identifier. |

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

Through the native Pixela API, this operation is `DELETE /v1/users/:username/graphs/:graphID` (base URL `https://pixe.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-graph.md) for the provider-specific parameters and requirements.

