# Ragic: Get Mass Task Status

Retrieves mass task status from Ragic.

```
GET https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-mass-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ragic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-mass-task-status?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-mass-task-status?${params}`, {
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
| `taskId` | string | yes | UUID returned by a Ragic mass operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ap": "string",
      "id": "string",
      "message": "string",
      "processed": 1,
      "status": "string",
      "taskName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ap` | string | Ragic application path that owns the task. |
| `id` | string | Mass-operation task identifier. |
| `message` | string | Ragic status message for the task. |
| `processed` | number | Number of processed records when provided by Ragic. |
| `status` | string | Current asynchronous task status. |
| `taskName` | string | Mass-operation task name. |

## Native endpoint

Through the native Ragic API, this operation is `GET /` (base URL `{{credentials.serverUrl}}/mindcloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mass-task-status.md) for the provider-specific parameters and requirements.

