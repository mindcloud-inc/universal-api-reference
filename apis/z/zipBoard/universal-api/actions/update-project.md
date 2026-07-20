# zipBoard: Update Project

Updates an existing project in zipBoard.

```
PUT https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collabEmail` | list<string> | no | Optional collaborator email list. |
| `description` | string | no | Updated project description. |
| `id` | string | yes | Project record ID to update. |
| `projectId` | string | no | Updated custom project ID. |
| `title` | string | no | Updated project title. |

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

Through the native zipBoard API, this operation is `PUT /projects/:id` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

