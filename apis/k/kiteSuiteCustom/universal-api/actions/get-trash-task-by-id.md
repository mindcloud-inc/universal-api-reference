# Kite Suite: Get trash task by ID



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-trash-task-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-trash-task-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-trash-task-by-id?${params}`, {
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
| `id` | string | yes | Task ID |

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

Through the native Kite Suite API, this operation is `GET /api/v1/task/trash/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trash-task-by-id.md) for the provider-specific parameters and requirements.

