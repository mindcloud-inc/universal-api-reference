# CAMB.AI: Get Audio Separation Task Status

Retrieves audio separation task status from CAMB.AI.

```
GET https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/get-audio-separation-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CAMB.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/get-audio-separation-task-status?connectionId=$CONNECTION_ID&task_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "task_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/get-audio-separation-task-status?${params}`, {
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
| `task_id` | string | yes | Task identifier returned by Create Audio Separation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exception_reason": "string",
      "message": "string",
      "run_id": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exception_reason` | string | Provider-supplied failure reason when the task does not complete successfully. |
| `message` | string | Optional provider message returned alongside the task status. |
| `run_id` | number | Run identifier available once the task succeeds. |
| `status` | string | Current status of the audio separation task. |

## Native endpoint

Through the native CAMB.AI API, this operation is `GET /audio-separation/:task_id` (base URL `https://client.camb.ai/apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audio-separation-task-status.md) for the provider-specific parameters and requirements.

