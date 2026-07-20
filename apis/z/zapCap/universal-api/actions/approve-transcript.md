# ZapCap: Approve Transcript

Approves a transcript for a ZapCap task.

```
PUT https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/approve-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZapCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/approve-transcript" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/approve-transcript', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoId` | string | yes | ZapCap video ID that owns the task. |
| `id` | string | yes | Caption task ID to approve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ZapCap API returns.

## Native endpoint

Through the native ZapCap API, this operation is `POST /videos/:videoId/task/:id/approve-transcript` (base URL `https://api.zapcap.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-transcript.md) for the provider-specific parameters and requirements.

