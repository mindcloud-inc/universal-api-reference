# zipBoard: Create Project

Creates a new project in zipBoard.

```
POST https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Project description. |
| `orgId` | string | no | Optional organization ID where the project should be created. |
| `projectId` | string | no | Optional custom project ID. |
| `title` | string | yes | Project title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "isEnabled": true,
      "orgId": "string",
      "projectId": "string",
      "screenCount": 1,
      "taskCount": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Project description. |
| `id` | string | Project identifier. |
| `isEnabled` | boolean | Whether the project is enabled. |
| `orgId` | string | Organization identifier. |
| `projectId` | string | Project code. |
| `screenCount` | number | Screen count. |
| `taskCount` | number | Task count. |
| `title` | string | Project title. |

## Native endpoint

Through the native zipBoard API, this operation is `POST /projects` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

