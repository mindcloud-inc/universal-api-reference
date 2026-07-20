# PiAPI/Luma (unofficial): Cancel Luma Tasks

Cancels Luma tasks in PiAPI created before a timestamp.

```
DELETE https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/cancel-luma-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Luma (unofficial) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/cancel-luma-tasks?connectionId=$CONNECTION_ID&createdBefore=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "createdBefore": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/cancel-luma-tasks?${params}`, {
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
| `createdBefore` | number | yes | Cancel pending Luma tasks created before this Unix timestamp. |

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
| `code` | number |  |
| `message` | string |  |

## Native endpoint

Through the native PiAPI/Luma (unofficial) API, this operation is `DELETE /api/v1/tasks` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-luma-tasks.md) for the provider-specific parameters and requirements.

