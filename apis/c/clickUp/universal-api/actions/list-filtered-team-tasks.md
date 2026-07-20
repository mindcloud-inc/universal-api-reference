# ClickUp: List Filtered Team Tasks

View the tasks that meet specific criteria from a Workspace.

```
GET https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-filtered-team-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-filtered-team-tasks?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-filtered-team-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customItems[]` | array<number> | no |  |
| `includeMarkdownDescription` | boolean | no |  |
| `teamId` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "creator": {
        "color": "string",
        "email": "ava@example.com",
        "id": 1,
        "profilePicture": "string",
        "username": "Ava Chen"
      },
      "customId": "string",
      "customItemId": 1,
      "dateClosed": "string",
      "dateCreated": "string",
      "dateDone": "string",
      "dateUpdated": "string",
      "description": "string",
      "dueDate": "string",
      "folder": {
        "access": true,
        "hidden": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "list": {
        "access": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "name": "Ava Chen",
      "orderindex": "string",
      "parent": "string",
      "permissionLevel": "string",
      "points": 1,
      "priority": "string",
      "project": {
        "access": true,
        "hidden": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "sharing": {
        "public": true,
        "publicFields": [
          "string"
        ],
        "publicShareExpiresOn": "string",
        "seoOptimized": true,
        "token": "string"
      },
      "space": {
        "id": "string"
      },
      "startDate": "string",
      "status": {
        "color": "string",
        "id": "string",
        "orderindex": 1,
        "status": "string",
        "type": "string"
      },
      "teamId": "string",
      "textContent": "string",
      "timeEstimate": 1,
      "topLevelParent": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `creator.color` | string |  |
| `creator.email` | string |  |
| `creator.id` | number |  |
| `creator.profilePicture` | string |  |
| `creator.username` | string |  |
| `customId` | string |  |
| `customItemId` | number |  |
| `dateClosed` | string |  |
| `dateCreated` | string |  |
| `dateDone` | string |  |
| `dateUpdated` | string |  |
| `description` | string |  |
| `dueDate` | string |  |
| `folder.access` | boolean |  |
| `folder.hidden` | boolean |  |
| `folder.id` | string |  |
| `folder.name` | string |  |
| `id` | string |  |
| `list.access` | boolean |  |
| `list.id` | string |  |
| `list.name` | string |  |
| `name` | string |  |
| `orderindex` | string |  |
| `parent` | string |  |
| `permissionLevel` | string |  |
| `points` | number |  |
| `priority` | string |  |
| `project.access` | boolean |  |
| `project.hidden` | boolean |  |
| `project.id` | string |  |
| `project.name` | string |  |
| `sharing.public` | boolean |  |
| `sharing.publicFields[]` | string |  |
| `sharing.publicShareExpiresOn` | string |  |
| `sharing.seoOptimized` | boolean |  |
| `sharing.token` | string |  |
| `space.id` | string |  |
| `startDate` | string |  |
| `status.color` | string |  |
| `status.id` | string |  |
| `status.orderindex` | number |  |
| `status.status` | string |  |
| `status.type` | string |  |
| `teamId` | string |  |
| `textContent` | string |  |
| `timeEstimate` | number |  |
| `topLevelParent` | string |  |
| `url` | string |  |

## Native endpoint

Through the native ClickUp API, this operation is `GET team/:team_Id/task` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-filtered-team-tasks.md) for the provider-specific parameters and requirements.

