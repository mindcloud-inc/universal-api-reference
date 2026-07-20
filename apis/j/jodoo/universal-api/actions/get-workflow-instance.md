# Jodoo: Get Workflow Instance



```
GET https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-workflow-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-workflow-instance?connectionId=$CONNECTION_ID&instanceId=63ff32d918fbc20007a4a082&tasksType=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "instanceId": "63ff32d918fbc20007a4a082",
  "tasksType": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-workflow-instance?${params}`, {
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
| `instanceId` | string | yes | Workflow instance ID, which is the same value as the workflow record data ID. Example: `63ff32d918fbc20007a4a082`. |
| `tasksType` | number | yes | Type of embedded task data to return. Use `0` to omit tasks or `1` to return all workflow tasks. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "createTime": "2026-05-07T12:00:00.000Z",
      "creator": {
        "departments": [
          1
        ],
        "name": "Ava Chen",
        "status": 1,
        "type": 1,
        "username": "Ava Chen"
      },
      "finishTime": "2026-05-07T12:00:00.000Z",
      "formId": "string",
      "formTitle": "string",
      "instanceId": "string",
      "status": 1,
      "tasks": [
        {
          "appId": "string",
          "assignee": {
            "departments": [
              1
            ],
            "name": "Ava Chen",
            "status": 1,
            "type": 1,
            "username": "Ava Chen"
          },
          "createAction": "string",
          "createTime": "2026-05-07T12:00:00.000Z",
          "creator": {
            "departments": [
              1
            ],
            "name": "Ava Chen",
            "status": 1,
            "type": 1,
            "username": "Ava Chen"
          },
          "finishAction": "string",
          "finishTime": "2026-05-07T12:00:00.000Z",
          "flowId": 1,
          "flowName": "Ava Chen",
          "formId": "string",
          "formTitle": "string",
          "instanceId": "string",
          "status": 1,
          "taskId": "string",
          "title": "string",
          "url": "https://example.com"
        }
      ],
      "updateTime": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `createTime` | date |  |
| `creator.departments[]` | number |  |
| `creator.name` | string |  |
| `creator.status` | number |  |
| `creator.type` | number |  |
| `creator.username` | string |  |
| `finishTime` | date |  |
| `formId` | string |  |
| `formTitle` | string |  |
| `instanceId` | string |  |
| `status` | number |  |
| `tasks[].appId` | string |  |
| `tasks[].assignee.departments[]` | number |  |
| `tasks[].assignee.name` | string |  |
| `tasks[].assignee.status` | number |  |
| `tasks[].assignee.type` | number |  |
| `tasks[].assignee.username` | string |  |
| `tasks[].createAction` | string |  |
| `tasks[].createTime` | date |  |
| `tasks[].creator.departments[]` | number |  |
| `tasks[].creator.name` | string |  |
| `tasks[].creator.status` | number |  |
| `tasks[].creator.type` | number |  |
| `tasks[].creator.username` | string |  |
| `tasks[].finishAction` | string |  |
| `tasks[].finishTime` | date |  |
| `tasks[].flowId` | number |  |
| `tasks[].flowName` | string |  |
| `tasks[].formId` | string |  |
| `tasks[].formTitle` | string |  |
| `tasks[].instanceId` | string |  |
| `tasks[].status` | number |  |
| `tasks[].taskId` | string |  |
| `tasks[].title` | string |  |
| `tasks[].url` | string |  |
| `updateTime` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Jodoo API, this operation is `POST https://api.jodoo.com/api/v6/workflow/instance/get` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-instance.md) for the provider-specific parameters and requirements.

