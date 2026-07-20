# TickTick: Update Project

Updates an existing project in TickTick.

```
PUT https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TickTick `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | list<string> | yes | Project identifier |
| `name` | string | no | Project name |
| `color` | string | no | Project color (hex) |
| `viewMode` | string | no | Project view mode |
| `kind` | string | no | Project kind |
| `sortOrder` | number | no | Project sort order |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "id": "string",
      "kind": "string",
      "name": "Ava Chen",
      "sortOrder": 1,
      "viewMode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `name` | string |  |
| `sortOrder` | number |  |
| `viewMode` | string |  |

## Native endpoint

Through the native TickTick API, this operation is `POST /open/v1/project/:projectId` (base URL `https://api.ticktick.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

