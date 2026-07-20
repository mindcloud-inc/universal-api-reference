# Everhour: Stop Timer

Stops the running timer in Everhour.

```
DELETE https://connect.mindcloud.co/v1/universal/everhour/latest/actions/stop-timer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everhour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/everhour/latest/actions/stop-timer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everhour/latest/actions/stop-timer?${params}`, {
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
      "comment": "string",
      "duration": 1,
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "task": {},
      "today": 1,
      "user": {},
      "userDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `duration` | number |  |
| `startedAt` | date |  |
| `status` | string |  |
| `task` | object |  |
| `today` | number |  |
| `user` | object |  |
| `userDate` | date |  |

## Native endpoint

Through the native Everhour API, this operation is `DELETE /timers/current` (base URL `https://api.everhour.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-timer.md) for the provider-specific parameters and requirements.

