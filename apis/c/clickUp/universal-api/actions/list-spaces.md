# ClickUp: List Spaces

View the Spaces available in a Workspace.

```
GET https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-spaces?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-spaces?${params}`, {
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
| `archived` | boolean | no |  |
| `teamId` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminCanManage": true,
      "archived": true,
      "avatar": "string",
      "color": "string",
      "features": {
        "checkUnresolved": {
          "checklists": {},
          "comments": {},
          "enabled": true,
          "subtasks": {}
        },
        "customFields": {
          "enabled": true
        },
        "customItems": {
          "enabled": true
        },
        "dependencyWarning": {
          "enabled": true
        },
        "dueDates": {
          "enabled": true,
          "remapClosedDueDate": true,
          "remapDueDates": true,
          "startDate": true
        },
        "emails": {
          "enabled": true
        },
        "milestones": {
          "enabled": true
        },
        "multipleAssignees": {
          "enabled": true
        },
        "points": {
          "enabled": true
        },
        "priorities": {
          "enabled": true,
          "priorities": [
            {
              "color": "string",
              "id": "string",
              "orderindex": "string",
              "priority": "string"
            }
          ]
        },
        "remapDependencies": {
          "enabled": true
        },
        "schedulerEnabled": true,
        "sprints": {
          "enabled": true
        },
        "statusPies": {
          "enabled": true
        },
        "tags": {
          "enabled": true
        },
        "timeEstimates": {
          "enabled": true,
          "perAssignee": true,
          "rollup": true
        },
        "timeTracking": {
          "defaultToBillable": 1,
          "enabled": true,
          "harvest": true,
          "rollup": true
        },
        "zoom": {
          "enabled": true
        }
      },
      "id": "string",
      "multipleAssignees": true,
      "name": "Ava Chen",
      "private": true,
      "statuses": [
        {
          "color": "string",
          "id": "string",
          "orderindex": 1,
          "status": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminCanManage` | boolean |  |
| `archived` | boolean |  |
| `avatar` | string |  |
| `color` | string |  |
| `features.checkUnresolved.checklists` | object |  |
| `features.checkUnresolved.comments` | object |  |
| `features.checkUnresolved.enabled` | boolean |  |
| `features.checkUnresolved.subtasks` | object |  |
| `features.customFields.enabled` | boolean |  |
| `features.customItems.enabled` | boolean |  |
| `features.dependencyWarning.enabled` | boolean |  |
| `features.dueDates.enabled` | boolean |  |
| `features.dueDates.remapClosedDueDate` | boolean |  |
| `features.dueDates.remapDueDates` | boolean |  |
| `features.dueDates.startDate` | boolean |  |
| `features.emails.enabled` | boolean |  |
| `features.milestones.enabled` | boolean |  |
| `features.multipleAssignees.enabled` | boolean |  |
| `features.points.enabled` | boolean |  |
| `features.priorities.enabled` | boolean |  |
| `features.priorities.priorities[].color` | string |  |
| `features.priorities.priorities[].id` | string |  |
| `features.priorities.priorities[].orderindex` | string |  |
| `features.priorities.priorities[].priority` | string |  |
| `features.remapDependencies.enabled` | boolean |  |
| `features.schedulerEnabled` | boolean |  |
| `features.sprints.enabled` | boolean |  |
| `features.statusPies.enabled` | boolean |  |
| `features.tags.enabled` | boolean |  |
| `features.timeEstimates.enabled` | boolean |  |
| `features.timeEstimates.perAssignee` | boolean |  |
| `features.timeEstimates.rollup` | boolean |  |
| `features.timeTracking.defaultToBillable` | number |  |
| `features.timeTracking.enabled` | boolean |  |
| `features.timeTracking.harvest` | boolean |  |
| `features.timeTracking.rollup` | boolean |  |
| `features.zoom.enabled` | boolean |  |
| `id` | string |  |
| `multipleAssignees` | boolean |  |
| `name` | string |  |
| `private` | boolean |  |
| `statuses[].color` | string |  |
| `statuses[].id` | string |  |
| `statuses[].orderindex` | number |  |
| `statuses[].status` | string |  |
| `statuses[].type` | string |  |

## Native endpoint

Through the native ClickUp API, this operation is `GET team/:team_id/space` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-spaces.md) for the provider-specific parameters and requirements.

