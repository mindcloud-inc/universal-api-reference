# SafetyCulture: List Actions

Retrieves actions from SafetyCulture.

```
GET https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/list-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/list-actions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/list-actions?${params}`, {
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
| `pageSize` | number | no | Optional. Number of actions to be returned in a single request. Maximum 100. Non-positive values are ignored. The presence of `next_page_token` in the response indicates that more results might be available. For example: '20'. |
| `pageToken` | string | no | Optional. If present, then retrieve the next batch of results from the preceding call to this method. `page_token` must be the value of `next_page_token` from the previous response. The values of other method parameters should be identical to those in the previous call. For example: 'ODFBMzQ3MDYtNzQxNy00RDZGLThDNjE1MEFDMkM4MTQ3NDQ='. |
| `inspectionId` | string | no | Optional. The ID of the inspection the action belongs to. Deprecated, inspectionID in `filters` should be used instead. |
| `offset` | number | no | Optional. Offset from where on the actions will be listed. |
| `sortField` | string | no | Optional. Which field to use for sorting. |
| `sortDirection` | string | no | Optional. Direction for sorting. |
| `withoutCount` | boolean | no | Optional. If true, will not return the count of actions. |
| `taskFilters[]` | array<object> | no | Optional. The array of filters to apply in your request. You can apply multiple filters in a single request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "task": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "dueAt": "2026-05-07T12:00:00.000Z",
        "priorityId": "string",
        "site": {
          "name": "Ava Chen"
        },
        "status": {
          "label": "string"
        },
        "taskId": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `task.createdAt` | date |  |
| `task.description` | string |  |
| `task.dueAt` | date |  |
| `task.priorityId` | string |  |
| `task.site.name` | string |  |
| `task.status.label` | string |  |
| `task.taskId` | string |  |
| `task.title` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `POST /tasks/v1/actions/list` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-actions.md) for the provider-specific parameters and requirements.

