# WotNot: Send API Visitor File Upload Response

Creates an API visitor file upload response in WotNot.

```
POST https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/send-api-visitor-file-upload-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WotNot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/send-api-visitor-file-upload-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "message.data.files[0].filename": "Ava Chen",
  "message.data.files[0].link": "https://example.com",
  "message.data.files[0].mime_type": "string",
  "message.data.files[0].extension": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/send-api-visitor-file-upload-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "message.data.files[0].filename": "Ava Chen",
    "message.data.files[0].link": "https://example.com",
    "message.data.files[0].mime_type": "string",
    "message.data.files[0].extension": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | API-channel conversation ID |
| `message.data.files[0].filename` | string | yes | Uploaded filename |
| `message.data.files[0].link` | string | yes | Public URL to the uploaded file |
| `message.data.files[0].mime_type` | string | yes | Uploaded file MIME type |
| `message.data.files[0].extension` | string | yes | Uploaded file extension |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WotNot API returns.

## Native endpoint

Through the native WotNot API, this operation is `POST /api/v1/conversation/:conversation_id/messages` (base URL `https://api.wotnot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-api-visitor-file-upload-response.md) for the provider-specific parameters and requirements.

