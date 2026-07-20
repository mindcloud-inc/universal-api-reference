# Taskade: Create Agent in Folder

Creates a new Taskade agent in a folder.

```
POST https://connect.mindcloud.co/v1/universal/taskade/latest/actions/create-agent-in-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Taskade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/taskade/latest/actions/create-agent-in-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "string",
  "name": "Ava Chen",
  "data.data.commands[].name": "Answer",
  "data.data.commands[].prompt": "Answer clearly and concisely.",
  "data.data.description": "Temporary test agent",
  "data.data.avatar.data.value": "🤖"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taskade/latest/actions/create-agent-in-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "string",
    "name": "Ava Chen",
    "data.data.commands[].name": "Answer",
    "data.data.commands[].prompt": "Answer clearly and concisely.",
    "data.data.description": "Temporary test agent",
    "data.data.avatar.data.value": "🤖"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | yes | Folder identifier from the path. |
| `name` | string | yes | Agent name. |
| `data.data.commands[].name` | string | yes | Single command display name. Example: `Answer`. |
| `data.data.commands[].prompt` | string | yes | Single command prompt text. Example: `Answer clearly and concisely.`. |
| `data.data.description` | string | yes | Agent description. Example: `Temporary test agent`. |
| `data.data.avatar.data.value` | string | yes | Avatar emoji value. Default: `🤖`. Example: `🤖`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "name": "Ava Chen",
      "spaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Agent configuration payload. |
| `id` | string | Agent ID. |
| `name` | string | Agent name. |
| `spaceId` | string | Folder or space ID. |

## Native endpoint

Through the native Taskade API, this operation is `POST /folders/:folderId/agents` (base URL `https://www.taskade.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent-in-folder.md) for the provider-specific parameters and requirements.

