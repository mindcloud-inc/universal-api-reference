# Pixela: Create Graph

Creates a new graph definition in Pixela.

```
POST https://connect.mindcloud.co/v1/universal/pixela/latest/actions/create-graph
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pixela `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pixela/latest/actions/create-graph" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "Ava Chen",
  "id": "string",
  "name": "Ava Chen",
  "unit": "string",
  "type": "string",
  "color": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixela/latest/actions/create-graph', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "Ava Chen",
    "id": "string",
    "name": "Ava Chen",
    "unit": "string",
    "type": "string",
    "color": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | yes | Pixela username in the request path. |
| `id` | string | yes | Graph ID. Must match ^[a-z][a-z0-9-]{1,16}. |
| `name` | string | yes | Graph display name. |
| `unit` | string | yes | Unit for recorded quantities, such as commit or kilogram. |
| `type` | string | yes | Quantity type. Pixela supports int or float. |
| `color` | string | yes | Graph color: shibafu, momiji, sora, ichou, ajisai, or kuro. |

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

Through the native Pixela API, this operation is `POST /v1/users/:username/graphs` (base URL `https://pixe.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-graph.md) for the provider-specific parameters and requirements.

