# Locu: Cancel Timer

Deletes the current timer from Locu.

```
DELETE https://connect.mindcloud.co/v1/universal/locu/latest/actions/cancel-timer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/locu/latest/actions/cancel-timer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/locu/latest/actions/cancel-timer?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "currentTaskId": "string",
      "duration": 1,
      "startedAt": "2026-05-07T12:00:00.000Z",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentTaskId` | string |  |
| `duration` | number |  |
| `startedAt` | date |  |
| `state` | string |  |

## Native endpoint

Through the native Locu API, this operation is `DELETE /timer` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-timer.md) for the provider-specific parameters and requirements.

