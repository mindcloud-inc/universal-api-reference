# DeskTime: Create Project

Creates a new project in DeskTime with an optional task.

```
POST https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeskTime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "MindCloud Sandbox"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "MindCloud Sandbox"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | yes | Project name. Example: `MindCloud Sandbox`. |
| `task` | string | no | Task name. Example: `Initial Task`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__request_time": "string",
      "project": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__request_time` | string |  |
| `project` | object |  |

## Native endpoint

Through the native DeskTime API, this operation is `POST /create-project` (base URL `https://desktime.com/api/v2/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

