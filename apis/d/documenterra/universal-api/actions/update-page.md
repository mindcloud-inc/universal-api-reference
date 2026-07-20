# Documenterra: Update Page

Updates an existing page in Documenterra.

```
PUT https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/update-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenterra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/update-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "topicId": "string",
  "updatedFields": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/update-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "topicId": "string",
    "updatedFields": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assigneeUserName` | string | no | Optional updated assignee username. |
| `body` | string | no | Updated page content body. |
| `indexKeywords[]` | array<string> | no | Optional updated page index keywords. |
| `ownerUserName` | string | no | Optional updated owner username. |
| `projectId` | string | yes | Documenterra project identifier. |
| `statusName` | string | no | Optional updated Documenterra status name. |
| `title` | string | no | Updated page title. |
| `topicId` | string | yes | Documenterra page identifier. |
| `updatedFields` | string | yes | Comma-separated list of page fields to update. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Documenterra API returns.

## Native endpoint

Through the native Documenterra API, this operation is `PATCH /projects/:projectId/articles/:topicId` (base URL `https://mindclouddocumenterra.try.documenterra.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page.md) for the provider-specific parameters and requirements.

