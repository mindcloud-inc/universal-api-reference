# ZapCap: Create Caption Task

Creates a caption task in ZapCap.

```
POST https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/create-caption-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZapCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/create-caption-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoId": "string",
  "templateId": "string",
  "autoApprove": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/create-caption-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoId": "string",
    "templateId": "string",
    "autoApprove": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoId` | string | yes | ZapCap video ID to process. |
| `templateId` | string | yes | Caption template ID from List Templates. |
| `autoApprove` | boolean | yes | Whether to skip manual transcript approval. |
| `language` | string | no | Language code for transcription. Default: `en`. Example: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskId` | string |  |

## Native endpoint

Through the native ZapCap API, this operation is `POST /videos/:videoId/task` (base URL `https://api.zapcap.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-caption-task.md) for the provider-specific parameters and requirements.

