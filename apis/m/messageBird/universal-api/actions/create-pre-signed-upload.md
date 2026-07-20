# MessageBird: Create Pre-Signed Upload



```
POST https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/create-pre-signed-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/create-pre-signed-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "conversationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/create-pre-signed-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "conversationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | string | yes | The Bird conversation ID for the upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mediaUrl": "https://example.com",
      "uploadFormData": {},
      "uploadMethod": "string",
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mediaUrl` | string | The URL to use when sending messages with this media. Must be passed in the `attachments` object. |
| `uploadFormData` | object | Form data fields that must be passed in addition to the field `file` when uploading the media to `uploadUrl`. |
| `uploadMethod` | string | The method to use when uploading the media, will always be POST. |
| `uploadUrl` | string | The URL to upload the media using form data encoding. The media must be sent with the field name `file` in addition to fields in `uploadFormData`. |

## Native endpoint

Through the native MessageBird API, this operation is `POST /workspaces/:workspaceId/conversations/:conversationId/presigned-upload` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pre-signed-upload.md) for the provider-specific parameters and requirements.

