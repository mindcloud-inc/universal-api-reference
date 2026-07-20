# Productive.io: Get Task

Retrieves a task from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-task?${params}`, {
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
| `id` | string | yes | The Productive resource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "billableTime": "string",
        "blockingDependencyCount": 1,
        "closed": true,
        "closedAt": "string",
        "createdAt": "string",
        "creationMethodId": 1,
        "customFields": "string",
        "deletedAt": "string",
        "description": "string",
        "dueDate": "string",
        "dueTime": "string",
        "emailKey": "ava@example.com",
        "initialEstimate": "string",
        "lastActivityAt": "string",
        "linkedDependencyCount": 1,
        "number": "string",
        "openSubtaskCount": "string",
        "openTodoCount": "string",
        "placement": 1,
        "private": true,
        "remainingTime": "string",
        "repeatOnDate": "string",
        "repeatOnInterval": "string",
        "repeatOnMonthday": "string",
        "repeatOnWeekday": [
          "string"
        ],
        "repeatOriginId": "string",
        "repeatScheduleId": "string",
        "startDate": "string",
        "subtaskCount": "string",
        "subtaskPlacement": "string",
        "tagList": [
          "string"
        ],
        "taskDependencyCount": 1,
        "taskNumber": "string",
        "title": "string",
        "todoAssigneeIds": [
          "string"
        ],
        "todoCount": "string",
        "typeId": 1,
        "updatedAt": "string",
        "waitingOnDependencyCount": 1,
        "workedTime": "string"
      },
      "id": "string",
      "relationships": {
        "assignee": {
          "meta": {
            "included": true
          }
        },
        "attachments": {
          "meta": {
            "included": true
          }
        },
        "creator": {
          "meta": {
            "included": true
          }
        },
        "customFieldAttachments": {
          "meta": {
            "included": true
          }
        },
        "customFieldPeople": {
          "meta": {
            "included": true
          }
        },
        "lastActor": {
          "meta": {
            "included": true
          }
        },
        "organization": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "parentTask": {
          "meta": {
            "included": true
          }
        },
        "project": {
          "meta": {
            "included": true
          }
        },
        "repeatedTask": {
          "meta": {
            "included": true
          }
        },
        "taskList": {
          "meta": {
            "included": true
          }
        },
        "templateObject": {
          "meta": {
            "included": true
          }
        },
        "workflowStatus": {
          "meta": {
            "included": true
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.billableTime` | string |  |
| `attributes.blockingDependencyCount` | number |  |
| `attributes.closed` | boolean |  |
| `attributes.closedAt` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.creationMethodId` | number |  |
| `attributes.customFields` | string |  |
| `attributes.deletedAt` | string |  |
| `attributes.description` | string |  |
| `attributes.dueDate` | string |  |
| `attributes.dueTime` | string |  |
| `attributes.emailKey` | string |  |
| `attributes.initialEstimate` | string |  |
| `attributes.lastActivityAt` | string |  |
| `attributes.linkedDependencyCount` | number |  |
| `attributes.number` | string |  |
| `attributes.openSubtaskCount` | string |  |
| `attributes.openTodoCount` | string |  |
| `attributes.placement` | number |  |
| `attributes.private` | boolean |  |
| `attributes.remainingTime` | string |  |
| `attributes.repeatOnDate` | string |  |
| `attributes.repeatOnInterval` | string |  |
| `attributes.repeatOnMonthday` | string |  |
| `attributes.repeatOnWeekday` | array<string> |  |
| `attributes.repeatOriginId` | string |  |
| `attributes.repeatScheduleId` | string |  |
| `attributes.startDate` | string |  |
| `attributes.subtaskCount` | string |  |
| `attributes.subtaskPlacement` | string |  |
| `attributes.tagList` | array<string> |  |
| `attributes.taskDependencyCount` | number |  |
| `attributes.taskNumber` | string |  |
| `attributes.title` | string |  |
| `attributes.todoAssigneeIds` | array<string> |  |
| `attributes.todoCount` | string |  |
| `attributes.typeId` | number |  |
| `attributes.updatedAt` | string |  |
| `attributes.waitingOnDependencyCount` | number |  |
| `attributes.workedTime` | string |  |
| `id` | string |  |
| `relationships.assignee.meta.included` | boolean |  |
| `relationships.attachments.meta.included` | boolean |  |
| `relationships.creator.meta.included` | boolean |  |
| `relationships.customFieldAttachments.meta.included` | boolean |  |
| `relationships.customFieldPeople.meta.included` | boolean |  |
| `relationships.lastActor.meta.included` | boolean |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.parentTask.meta.included` | boolean |  |
| `relationships.project.meta.included` | boolean |  |
| `relationships.repeatedTask.meta.included` | boolean |  |
| `relationships.taskList.meta.included` | boolean |  |
| `relationships.templateObject.meta.included` | boolean |  |
| `relationships.workflowStatus.meta.included` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /tasks/{{id}}` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

