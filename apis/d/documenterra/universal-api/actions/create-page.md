# Documenterra: Create Page

Creates a page in Documenterra.

```
POST https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/create-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenterra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/create-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assigneeUserName": "Ava Chen",
  "id": "string",
  "ownerUserName": "Ava Chen",
  "projectId": "string",
  "statusName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/create-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assigneeUserName": "Ava Chen",
    "id": "string",
    "ownerUserName": "Ava Chen",
    "projectId": "string",
    "statusName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assigneeUserName` | string | yes | Optional assignee username. |
| `body` | string | no | Page content body. |
| `id` | string | yes | Optional page identifier to assign during creation. |
| `indexKeywords[]` | array<string> | no | Optional page index keywords. |
| `isShowInToc` | boolean | no | Whether to show the page in the tree of contents. |
| `ownerUserName` | string | yes | Optional owner username. |
| `parentTocNodeId` | string | no | Optional parent tree node identifier. |
| `projectId` | string | yes | Documenterra project identifier. |
| `statusName` | string | yes | Optional Documenterra status name. |
| `title` | string | no | Page title. |
| `tocNodeCaption` | string | no | Optional tree caption for the page node. |
| `tocNodeOrdinalNo` | number | no | Optional tree order index for the page node. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Documenterra API returns.

## Native endpoint

Through the native Documenterra API, this operation is `POST /projects/:projectId/articles` (base URL `https://mindclouddocumenterra.try.documenterra.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-page.md) for the provider-specific parameters and requirements.

