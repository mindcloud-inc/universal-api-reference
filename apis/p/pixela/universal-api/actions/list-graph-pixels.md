# Pixela: List Graph Pixels

Retrieves pixels from a Pixela graph by date range.

```
GET https://connect.mindcloud.co/v1/universal/pixela/latest/actions/list-graph-pixels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pixela `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixela/latest/actions/list-graph-pixels?connectionId=$CONNECTION_ID&username=Ava%20Chen&graph_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen",
  "graph_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixela/latest/actions/list-graph-pixels?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | no | Start date in yyyyMMdd format. |
| `to` | string | no | End date in yyyyMMdd format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pixels": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pixels` | array<string> | Pixel dates in yyyyMMdd format. |

## Native endpoint

Through the native Pixela API, this operation is `GET /v1/users/:username/graphs/:graphID/pixels` (base URL `https://pixe.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-graph-pixels.md) for the provider-specific parameters and requirements.

