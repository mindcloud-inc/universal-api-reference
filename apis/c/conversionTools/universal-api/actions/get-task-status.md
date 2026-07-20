# Conversion Tools: Get Task Status

Retrieves the current status of a conversion task from Conversion Tools.

```
GET https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/get-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conversion Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/get-task-status?connectionId=$CONNECTION_ID&taskId=28f2f333593949fe9b33c859c6d339de" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "28f2f333593949fe9b33c859c6d339de"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/get-task-status?${params}`, {
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
| `taskId` | string | yes | The task ID returned by task creation. Example: `28f2f333593949fe9b33c859c6d339de`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversionProgress": 1,
      "conversionResult": {},
      "error": "string",
      "file_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversionProgress` | number | Provider conversion progress percentage when available. |
| `conversionResult` | object | Provider conversion result details. |
| `error` | string | Provider error message when present. |
| `file_id` | string | Result file ID when the task succeeds. |
| `status` | string | Current provider task status. |

## Native endpoint

Through the native Conversion Tools API, this operation is `GET /tasks/:taskId` (base URL `https://api.conversiontools.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-status.md) for the provider-specific parameters and requirements.

