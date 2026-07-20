# Pixela: Get Graph Stats

Retrieves statistics for a Pixela graph.

```
GET https://connect.mindcloud.co/v1/universal/pixela/latest/actions/get-graph-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pixela `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixela/latest/actions/get-graph-stats?connectionId=$CONNECTION_ID&username=Ava%20Chen&graph_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen",
  "graph_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixela/latest/actions/get-graph-stats?${params}`, {
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
      "avgQuantity": 1,
      "maxDate": "string",
      "maxQuantity": 1,
      "minDate": "string",
      "minQuantity": 1,
      "todaysQuantity": 1,
      "totalPixelsCount": 1,
      "totalQuantity": 1,
      "yesterdayQuantity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avgQuantity` | number |  |
| `maxDate` | string |  |
| `maxQuantity` | number |  |
| `minDate` | string |  |
| `minQuantity` | number |  |
| `todaysQuantity` | number |  |
| `totalPixelsCount` | number |  |
| `totalQuantity` | number |  |
| `yesterdayQuantity` | number |  |

## Native endpoint

Through the native Pixela API, this operation is `GET /v1/users/:username/graphs/:graphID/stats` (base URL `https://pixe.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-graph-stats.md) for the provider-specific parameters and requirements.

