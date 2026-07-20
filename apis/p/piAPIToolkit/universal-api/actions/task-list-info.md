# PiAPI/Toolkit: Task List Info

Retrieves active task counts from PiAPI/Toolkit.

```
GET https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/task-list-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Toolkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/task-list-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/task-list-info?${params}`, {
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
      "flux": {
        "pending_count": 1,
        "processing_count": 1,
        "staged_count": 1
      },
      "kling": {
        "pending_count": 1,
        "processing_count": 1,
        "staged_count": 1
      },
      "luma": {
        "pending_count": 1,
        "processing_count": 1,
        "staged_count": 1
      },
      "midjourney": {
        "pending_count": 1,
        "processing_count": 1,
        "staged_count": 1
      },
      "music-s": {
        "pending_count": 1,
        "processing_count": 1,
        "staged_count": 1
      },
      "music-u": {
        "pending_count": 1,
        "processing_count": 1,
        "staged_count": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `flux.pending_count` | number |  |
| `flux.processing_count` | number |  |
| `flux.staged_count` | number |  |
| `kling.pending_count` | number |  |
| `kling.processing_count` | number |  |
| `kling.staged_count` | number |  |
| `luma.pending_count` | number |  |
| `luma.processing_count` | number |  |
| `luma.staged_count` | number |  |
| `midjourney.pending_count` | number |  |
| `midjourney.processing_count` | number |  |
| `midjourney.staged_count` | number |  |
| `music-s.pending_count` | number |  |
| `music-s.processing_count` | number |  |
| `music-s.staged_count` | number |  |
| `music-u.pending_count` | number |  |
| `music-u.processing_count` | number |  |
| `music-u.staged_count` | number |  |

## Native endpoint

Through the native PiAPI/Toolkit API, this operation is `GET /account/active_tasks` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/task-list-info.md) for the provider-specific parameters and requirements.

