# Ringg AI: Create Knowledge Base

Creates a knowledge base in Ringg AI.

```
POST https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/create-knowledge-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/create-knowledge-base" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "kbName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/create-knowledge-base', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "kbName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `kbName` | string | yes | (Required) Name of the knowledge base |
| `files[]` | array<string> | no | (Optional) Array of files to upload (max 10 files, 2 MB each, 5 MB total) |
| `urls` | string | no | (Optional) JSON string array of URLs to index (max 20 URLs) |
| `faqs` | string | no | (Optional) JSON string array of FAQ objects |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filesQueued": 1,
      "kbId": "string",
      "message": "string",
      "processingStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filesQueued` | number |  |
| `kbId` | string |  |
| `message` | string |  |
| `processingStatus` | string |  |

## Native endpoint

Through the native Ringg AI API, this operation is `POST /external/kb` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-knowledge-base.md) for the provider-specific parameters and requirements.

