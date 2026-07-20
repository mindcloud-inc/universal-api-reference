# SafetyCulture: List Issues

Retrieves issues from SafetyCulture.

```
GET https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/list-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/list-issues?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/list-issues?${params}`, {
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
| `pageSize` | number | no | Optional. Number of issues to be returned in a single request. This must be a value between 1 and 100, any values outside of this range will be ignored. The presence of `next_page_token` in the response indicates that more results might be available. |
| `pageToken` | string | no | Optional. If present, then retrieve the next batch of results from the preceding call to this method. `page_token` must be the value of `next_page_token` from the previous response. The values of other method parameters should be identical to those in the previous call. This can be used to retrieve more than 100 issues with multiple API calls. For example: 'ODFBMzQ3MDYtNzQxNy00RDZGLThDNjE1MEFDMkM4MTQ3NDQ=' |
| `sortField` | string | no | Optional. Which field to use for sorting. |
| `sortDirection` | string | no | Optional. Direction for sorting. |
| `filters[]` | array<object> | no | Optional. An array of filters can be provided in the request to filter the issues. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": "string",
      "task": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "dueAt": "2026-05-07T12:00:00.000Z",
        "priorityId": "string",
        "statusId": "string",
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
| `categoryId` | string |  |
| `task.createdAt` | date |  |
| `task.description` | string |  |
| `task.dueAt` | date |  |
| `task.priorityId` | string |  |
| `task.statusId` | string |  |
| `task.taskId` | string |  |
| `task.title` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `POST /tasks/v1/incidents/list` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-issues.md) for the provider-specific parameters and requirements.

