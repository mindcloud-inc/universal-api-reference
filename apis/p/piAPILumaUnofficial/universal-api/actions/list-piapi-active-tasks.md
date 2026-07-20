# PiAPI/Luma (unofficial): Get PiAPI Active Tasks

Retrieves active task counts from PiAPI.

```
GET https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/list-piapi-active-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Luma (unofficial) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/list-piapi-active-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/list-piapi-active-tasks?${params}`, {
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
      "code": 1,
      "data": {
        "flux": {},
        "kling": {},
        "luma": {},
        "midjourney": {}
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | PiAPI status code. |
| `data` | object | Active-task counts grouped by provider family. |
| `data.flux` | object | Flux active-task counters. |
| `data.kling` | object | Kling active-task counters. |
| `data.luma` | object | Luma active-task counters. |
| `data.midjourney` | object | Midjourney active-task counters. |
| `message` | string | PiAPI status message. |

## Native endpoint

Through the native PiAPI/Luma (unofficial) API, this operation is `GET /account/active_tasks` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-piapi-active-tasks.md) for the provider-specific parameters and requirements.

