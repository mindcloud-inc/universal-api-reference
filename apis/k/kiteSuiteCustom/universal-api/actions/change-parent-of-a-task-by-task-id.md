# Kite Suite: change parent of a task by task Id



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/change-parent-of-a-task-by-task-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/change-parent-of-a-task-by-task-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "parentTask": "string",
  "taskID": "string",
  "isSubIssue": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/change-parent-of-a-task-by-task-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "parentTask": "string",
    "taskID": "string",
    "isSubIssue": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `parentTask` | string | yes |  |
| `taskID` | string | yes |  |
| `isSubIssue` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "activity": [
        "string"
      ],
      "assigneeID": "string",
      "attachment": "string",
      "customFields": [
        "string"
      ],
      "description": "string",
      "dueDate": "string",
      "epic": "string",
      "flag": true,
      "isSubTask": true,
      "issueType": "string",
      "isTrashed": true,
      "labels": [
        "string"
      ],
      "linkIssues": [
        "https://example.com"
      ],
      "listID": "string",
      "parentTask": "string",
      "priority": "string",
      "projectID": "string",
      "reporter": "string",
      "SN": "string",
      "sprint": "string",
      "storyPointEstimate": 1,
      "subTask": [
        "string"
      ],
      "summary": "string",
      "voted": [
        "string"
      ],
      "watched": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the task |
| `activity` | array | activity of task |
| `assigneeID` | string | assignee to task |
| `attachment` | string | array of attachment |
| `customFields` | array | custom fields of task |
| `description` | string | Description of task |
| `dueDate` | string | due date of the task |
| `epic` | string | epic id of the task |
| `flag` | boolean | flag of this task |
| `isSubTask` | boolean |  |
| `issueType` | string | Issue type like epic,story,task,bug |
| `isTrashed` | boolean | trash status of this task |
| `labels` | array | labels of this task |
| `linkIssues` | array | link of task |
| `listID` | string | List ID of project |
| `parentTask` | string | parent task id of the task |
| `priority` | string | Priority like high,medium,low,none |
| `projectID` | string | project ID of project |
| `reporter` | string | reporter of the this task |
| `SN` | string | Serial Number of the task |
| `sprint` | string | Sprint of this task |
| `storyPointEstimate` | number | estimation of this task |
| `subTask` | array | array of sub task |
| `summary` | string | summary of task |
| `voted` | array | array of voted user |
| `watched` | array | array of wached user |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/task/convert` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-parent-of-a-task-by-task-id.md) for the provider-specific parameters and requirements.

