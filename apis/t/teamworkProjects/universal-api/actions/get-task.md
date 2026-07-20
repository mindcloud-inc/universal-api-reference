# Teamwork Projects: Get Task

Retrieves detailed task information from Teamwork Projects.

```
GET https://connect.mindcloud.co/v1/universal/teamworkProjects/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamwork Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamworkProjects/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamworkProjects/latest/actions/get-task?${params}`, {
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
| `taskId` | number | yes | Teamwork task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "included": {},
      "meta": {},
      "task": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `included` | object | Included related resources keyed by type. |
| `meta` | object | Response metadata. |
| `task` | object | The requested Teamwork task. |

## Native endpoint

Through the native Teamwork Projects API, this operation is `GET /tasks/{{taskId}}.json` (base URL `{{credentials.accessTokenRequest.installation.apiEndPoint}}projects/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

