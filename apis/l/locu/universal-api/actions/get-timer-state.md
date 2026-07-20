# Locu: Get Timer State

Retrieves the current timer state from Locu.

```
GET https://connect.mindcloud.co/v1/universal/locu/latest/actions/get-timer-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/locu/latest/actions/get-timer-state?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/locu/latest/actions/get-timer-state?${params}`, {
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

Through the native Locu API, this operation is `GET /timer` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-timer-state.md) for the provider-specific parameters and requirements.

