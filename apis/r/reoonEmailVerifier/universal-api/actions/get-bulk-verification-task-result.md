# Reoon Email Verifier: Get Bulk Verification Task Result



```
GET https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/get-bulk-verification-task-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reoon Email Verifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/get-bulk-verification-task-result?connectionId=$CONNECTION_ID&taskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/get-bulk-verification-task-result?${params}`, {
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
| `taskId` | number | yes | The bulk verification task id returned by Reoon. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count_checked": 1,
      "count_total": 1,
      "name": "Ava Chen",
      "progress_percentage": 1,
      "results": {},
      "status": "string",
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count_checked` | number |  |
| `count_total` | number |  |
| `name` | string |  |
| `progress_percentage` | number |  |
| `results` | object |  |
| `status` | string |  |
| `task_id` | string |  |

## Native endpoint

Through the native Reoon Email Verifier API, this operation is `GET /get-result-bulk-verification-task/` (base URL `https://emailverifier.reoon.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-verification-task-result.md) for the provider-specific parameters and requirements.

