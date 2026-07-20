# PiAPI/Flux.1: List Active Tasks

Retrieves active task records from PiAPI/Flux.1.

```
GET https://connect.mindcloud.co/v1/universal/piAPIFlux1/latest/actions/list-active-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Flux.1 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIFlux1/latest/actions/list-active-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIFlux1/latest/actions/list-active-tasks?${params}`, {
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
        "flux": {
          "active_tasks": [
            {}
          ],
          "pending_count": 1,
          "processing_count": 1,
          "staged_count": 1
        }
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
| `code` | number |  |
| `data.flux.active_tasks` | array<object> |  |
| `data.flux.pending_count` | number |  |
| `data.flux.processing_count` | number |  |
| `data.flux.staged_count` | number |  |
| `message` | string |  |

## Native endpoint

Through the native PiAPI/Flux.1 API, this operation is `GET /account/active_tasks` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-tasks.md) for the provider-specific parameters and requirements.

