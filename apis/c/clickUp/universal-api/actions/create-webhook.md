# ClickUp: Create Webhook

Creates a webhook in ClickUp for selected events.

```
POST https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endpoint": "string",
  "events": "*",
  "teamID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endpoint": "string",
    "events": "*",
    "teamID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endpoint` | string | yes |  |
| `events` | list<string> | yes | One of: `*`, `folderCreated`, `folderDeleted`, `folderUpdated`, `goalCreated`, `goalDeleted`, `goalUpdated`, `keyResultCreated`, `keyResultDeleted`, `keyResultUpdated`, `listCreated`, `listDeleted`, `listUpdated`, `spaceCreated`, `spaceDeleted`, `spaceUpdated`, `taskAssigneeUpdated`, `taskCommentPosted`, `taskCommentUpdated`, `taskCreated`, `taskDeleted`, `taskDueDateUpdated`, `taskMoved`, `taskPriorityUpdated`, `taskStatusUpdated`, `taskTagUpdated`, `taskTimeEstimateUpdated`, `taskTimeTrackedUpdated`, `taskUpdated`. Accepts multiple values as an array. |
| `folderId` | number | no |  |
| `listId` | number | no |  |
| `spaceId` | number | no |  |
| `taskId` | string | no |  |
| `teamID` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "webhook": {
        "clientId": "string",
        "endpoint": "string",
        "events": [
          "string"
        ],
        "folderId": "string",
        "health": {
          "failCount": 1,
          "status": "string"
        },
        "id": "string",
        "listId": "string",
        "secret": "string",
        "spaceId": "string",
        "taskId": "string",
        "teamId": 1,
        "userid": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `webhook` | object |  |
| `webhook.clientId` | string |  |
| `webhook.endpoint` | string |  |
| `webhook.events` | array |  |
| `webhook.events[]` | string |  |
| `webhook.folderId` | string |  |
| `webhook.health` | object |  |
| `webhook.health.failCount` | number |  |
| `webhook.health.status` | string |  |
| `webhook.id` | string |  |
| `webhook.listId` | string |  |
| `webhook.secret` | string |  |
| `webhook.spaceId` | string |  |
| `webhook.taskId` | string |  |
| `webhook.teamId` | number |  |
| `webhook.userid` | number |  |

## Native endpoint

Through the native ClickUp API, this operation is `POST team/:team_id/webhook` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

