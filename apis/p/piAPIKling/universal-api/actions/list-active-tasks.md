# PiAPI/Kling: List Active Tasks



```
GET https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/list-active-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Kling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/list-active-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/list-active-tasks?${params}`, {
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
      "flux": {},
      "kling": {},
      "luma": {},
      "midjourney": {},
      "musicS": {},
      "musicU": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `flux` | object | Active task counts for Flux. |
| `kling` | object | Active task counts for Kling. |
| `luma` | object | Active task counts for Luma. |
| `midjourney` | object | Active task counts for Midjourney. |
| `musicS` | object | Active task counts for Music-S. |
| `musicU` | object | Active task counts for Music-U. |

## Native endpoint

Through the native PiAPI/Kling API, this operation is `GET /account/active_tasks` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-tasks.md) for the provider-specific parameters and requirements.

