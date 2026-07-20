# ZapCap: Get Viral Clip Task Status

Retrieves clip task status from ZapCap.

```
GET https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/get-viral-clip-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZapCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/get-viral-clip-task-status?connectionId=$CONNECTION_ID&videoId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/get-viral-clip-task-status?${params}`, {
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
| `videoId` | string | yes | ZapCap video ID. |
| `id` | string | yes | ZapCap clip task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clips": [
        {
          "theme": "string",
          "url": "https://example.com"
        }
      ],
      "error": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clips[].theme` | string | Provider-supplied clip theme. |
| `clips[].url` | string | Generated clip download URL. |
| `error` | string | Failure reason when present. |
| `id` | string | ZapCap clip task ID. |
| `status` | string | Current clip task status. |

## Native endpoint

Through the native ZapCap API, this operation is `GET /videos/:videoId/clipTask/:id` (base URL `https://api.zapcap.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-viral-clip-task-status.md) for the provider-specific parameters and requirements.

