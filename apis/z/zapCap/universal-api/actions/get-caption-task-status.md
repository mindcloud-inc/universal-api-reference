# ZapCap: Get Caption Task Status

Retrieves caption task status from ZapCap.

```
GET https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/get-caption-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZapCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/get-caption-task-status?connectionId=$CONNECTION_ID&videoId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/get-caption-task-status?${params}`, {
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
| `videoId` | string | yes | ZapCap video ID that owns the task. |
| `id` | string | yes | Caption task ID to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brolls": {},
      "downloadUrl": "https://example.com",
      "id": "string",
      "status": "string",
      "storageIds": {
        "original": "string",
        "render": "string",
        "transcript": "string"
      },
      "transcript": "string",
      "transcriptApproved": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brolls` | object |  |
| `downloadUrl` | string |  |
| `id` | string |  |
| `status` | string |  |
| `storageIds.original` | string |  |
| `storageIds.render` | string |  |
| `storageIds.transcript` | string |  |
| `transcript` | string |  |
| `transcriptApproved` | boolean |  |

## Native endpoint

Through the native ZapCap API, this operation is `GET /videos/:videoId/task/:id` (base URL `https://api.zapcap.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-caption-task-status.md) for the provider-specific parameters and requirements.

