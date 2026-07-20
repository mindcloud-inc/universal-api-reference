# Zeplin: Create Project Color

Creates a new project color in Zeplin.

```
POST https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/create-project-color
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/create-project-color" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "name": "Ava Chen",
  "sourceId": "string",
  "r": 1,
  "g": 1,
  "b": 1,
  "a": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/create-project-color', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "name": "Ava Chen",
    "sourceId": "string",
    "r": 1,
    "g": 1,
    "b": 1,
    "a": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Project id |
| `name` | string | yes | Name of the color |
| `sourceId` | string | yes | Color's identifier in the design tool |
| `r` | number | yes | Red component of the color |
| `g` | number | yes | Green component of the color |
| `b` | number | yes | Blue component of the color |
| `a` | number | yes | Alpha component of the color |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Zeplin API, this operation is `POST /projects/{project_id}/colors` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-color.md) for the provider-specific parameters and requirements.

