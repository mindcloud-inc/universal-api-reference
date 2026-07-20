# Roborabbit: Retrieve Run

Retrieves a run for a specific Roborabbit task.

```
GET https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/retrieve-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Roborabbit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/retrieve-run?connectionId=$CONNECTION_ID&taskUid=string&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskUid": "string",
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/retrieve-run?${params}`, {
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
| `taskUid` | string | yes | The parent task UID. |
| `uid` | string | yes | The run UID from Roborabbit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "finishedInSeconds": 1,
      "metadata": "string",
      "outputs": [
        "string"
      ],
      "status": "string",
      "steps": [
        {}
      ],
      "task": "string",
      "uid": "string",
      "videoUrl": "https://example.com",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `finishedInSeconds` | number |  |
| `metadata` | string |  |
| `outputs` | array |  |
| `status` | string |  |
| `steps` | array<object> |  |
| `task` | string |  |
| `uid` | string |  |
| `videoUrl` | string |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Roborabbit API, this operation is `GET /v1/tasks/:task_uid/runs/:uid` (base URL `https://api.roborabbit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-run.md) for the provider-specific parameters and requirements.

