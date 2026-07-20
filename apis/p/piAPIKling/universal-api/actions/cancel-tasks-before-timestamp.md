# PiAPI/Kling: Cancel Tasks Before Timestamp



```
DELETE https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/cancel-tasks-before-timestamp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Kling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/cancel-tasks-before-timestamp?connectionId=$CONNECTION_ID&createdBefore=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "createdBefore": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/cancel-tasks-before-timestamp?${params}`, {
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
| `createdBefore` | number | yes | Unix timestamp in seconds. Cancel pending Kling tasks created before this time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | PiAPI response code. |
| `message` | string | Provider bulk cancellation result message. |

## Native endpoint

Through the native PiAPI/Kling API, this operation is `DELETE /api/v1/tasks` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-tasks-before-timestamp.md) for the provider-specific parameters and requirements.

