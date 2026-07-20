# ArcSite: Remove Project Collaborators

Removes collaborators from an existing ArcSite project.

```
PUT https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/remove-project-collaborators
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ArcSite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/remove-project-collaborators" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/remove-project-collaborators', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "emails[]": ["ava@example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The ID of the project. |
| `emails[]` | array<string> | yes | Collaborator emails to remove. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ArcSite API returns.

## Native endpoint

Through the native ArcSite API, this operation is `POST /projects/:projectId/remove_collaborators` (base URL `https://api.arcsite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-project-collaborators.md) for the provider-specific parameters and requirements.

