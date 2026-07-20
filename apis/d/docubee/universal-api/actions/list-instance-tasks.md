# Docubee: List Instance Tasks

Retrieves tasks for a Docubee workflow instance.

```
GET https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-instance-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-instance-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-instance-tasks?${params}`, {
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
| `instanceId` | string | no | The workflow instance ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": "string",
      "participant": "string",
      "status": "string",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | string | The task label. |
| `participant` | string | The task participant. |
| `status` | string | The task status. |
| `taskId` | string | The task ID. |

## Native endpoint

Through the native Docubee API, this operation is `GET /instances/:instanceId/tasks` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-instance-tasks.md) for the provider-specific parameters and requirements.

