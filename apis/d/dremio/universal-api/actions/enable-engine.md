# Dremio: Enable Engine

Enables an engine in a Dremio project.

```
PUT https://connect.mindcloud.co/v1/universal/dremio/latest/actions/enable-engine
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/enable-engine" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dremio/latest/actions/enable-engine', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeReplicas": 1,
      "engineType": "string",
      "id": "string",
      "name": "Ava Chen",
      "size": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeReplicas` | number |  |
| `engineType` | string |  |
| `id` | string |  |
| `name` | string |  |
| `size` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Dremio API, this operation is `PUT /projects/:project_id/engines/:id/enable` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enable-engine.md) for the provider-specific parameters and requirements.

