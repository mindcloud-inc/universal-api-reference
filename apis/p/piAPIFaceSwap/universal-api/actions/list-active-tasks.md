# PiAPI/FaceSwap: List Active Tasks

Retrieves active task counts from PiAPI/FaceSwap.

```
GET https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/list-active-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/FaceSwap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/list-active-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/list-active-tasks?${params}`, {
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
        "midjourney": {},
        "music-s": {},
        "music-u": {}
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
| `code` | number | PiAPI response code. |
| `data` | object | Active task counts grouped by provider family. |
| `data.flux` | object | Active Flux task counters. |
| `data.kling` | object | Active Kling task counters. |
| `data.luma` | object | Active Luma task counters. |
| `data.midjourney` | object | Active Midjourney task counters. |
| `data.music-s` | object | Active music-s task counters. |
| `data.music-u` | object | Active music-u task counters. |
| `message` | string | PiAPI response message. |

## Native endpoint

Through the native PiAPI/FaceSwap API, this operation is `GET /account/active_tasks` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-tasks.md) for the provider-specific parameters and requirements.

