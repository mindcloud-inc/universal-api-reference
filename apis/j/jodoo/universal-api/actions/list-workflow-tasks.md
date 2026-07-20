# Jodoo: List Workflow Tasks



```
GET https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/list-workflow-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/list-workflow-tasks?connectionId=$CONNECTION_ID&username=jdy-57q312f65pz7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "jdy-57q312f65pz7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/list-workflow-tasks?${params}`, {
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
| `username` | string | yes | Username whose pending workflow tasks should be listed. Example: `jdy-57q312f65pz7`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | Number of workflow tasks to skip. Example: `0`. |
| `limit` | number | no | Maximum number of workflow tasks to return. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `assignee.departments[]` | number |  |
| `assignee.name` | string |  |
| `assignee.status` | number |  |
| `assignee.type` | number |  |
| `assignee.username` | string |  |
| `createAction` | string |  |
| `createTime` | date |  |
| `creator.departments[]` | number |  |
| `creator.name` | string |  |
| `creator.status` | number |  |
| `creator.type` | number |  |
| `creator.username` | string |  |
| `finishAction` | string |  |
| `finishTime` | date |  |
| `flowId` | number |  |
| `flowName` | string |  |
| `formId` | string |  |
| `formTitle` | string |  |
| `instanceId` | string |  |
| `status` | number |  |
| `taskId` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Jodoo API, this operation is `POST https://api.jodoo.com/api/v4/workflow/task/list` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-tasks.md) for the provider-specific parameters and requirements.

