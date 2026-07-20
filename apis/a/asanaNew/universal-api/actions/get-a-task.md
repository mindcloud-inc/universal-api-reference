# Asana: Get a task

Retrieves a task from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-a-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-a-task?connectionId=$CONNECTION_ID&taskGid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskGid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-a-task?${params}`, {
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
| `taskGid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualTimeMinutes": {},
      "assignee": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "assigneeSection": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "assigneeStatus": "string",
      "completed": true,
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dueAt": "2026-05-07T12:00:00.000Z",
      "dueOn": "2026-05-07T12:00:00.000Z",
      "followers": [
        {
          "gid": "string",
          "name": "Ava Chen",
          "resourceType": "string"
        }
      ],
      "gid": "string",
      "hearted": true,
      "liked": true,
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "notes": "string",
      "numHearts": 1,
      "numLikes": 1,
      "parent": {},
      "permalinkUrl": "https://example.com",
      "resourceSubtype": "string",
      "resourceType": "string",
      "startAt": "2026-05-07T12:00:00.000Z",
      "startOn": "2026-05-07T12:00:00.000Z",
      "workspace": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualTimeMinutes` | object |  |
| `assignee.gid` | string |  |
| `assignee.name` | string |  |
| `assignee.resourceType` | string |  |
| `assigneeSection.gid` | string |  |
| `assigneeSection.name` | string |  |
| `assigneeSection.resourceType` | string |  |
| `assigneeStatus` | string |  |
| `completed` | boolean |  |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `dueAt` | date |  |
| `dueOn` | date |  |
| `followers[].gid` | string |  |
| `followers[].name` | string |  |
| `followers[].resourceType` | string |  |
| `gid` | string |  |
| `hearted` | boolean |  |
| `liked` | boolean |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `notes` | string |  |
| `numHearts` | number |  |
| `numLikes` | number |  |
| `parent` | object |  |
| `permalinkUrl` | string |  |
| `resourceSubtype` | string |  |
| `resourceType` | string |  |
| `startAt` | date |  |
| `startOn` | date |  |
| `workspace.gid` | string |  |
| `workspace.name` | string |  |
| `workspace.resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `GET tasks/:task_gid` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-task.md) for the provider-specific parameters and requirements.

