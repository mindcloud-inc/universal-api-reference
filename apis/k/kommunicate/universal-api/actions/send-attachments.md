# Kommunicate: Send Attachments

Creates an attachment message in Kommunicate.

```
POST https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/send-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kommunicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/send-attachments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ofUserId": "string",
  "type": 1,
  "contentType": 1,
  "groupId": "string",
  "key": "string",
  "fileMeta": {},
  "source": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/send-attachments', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ofUserId": "string",
    "type": 1,
    "contentType": 1,
    "groupId": "string",
    "key": "string",
    "fileMeta": {},
    "source": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ofUserId` | string | yes | Admin user email to route into the required Of-User-Id header. |
| `type` | number | yes | Attachment type value from Kommunicate. |
| `contentType` | number | yes | Kommunicate content type code for the attachment message. |
| `message` | string | no | Optional attachment caption or description. |
| `groupId` | string | yes | Conversation identifier to send the attachment into. |
| `metadata` | object | no | Optional attachment metadata, for example skipBot. |
| `key` | string | yes | Kommunicate attachment key. |
| `fileMeta` | object | yes | File metadata object including blobKey and contentType. |
| `source` | number | yes | Kommunicate source value for the attachment message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "messageKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `messageKey` | string |  |

## Native endpoint

Through the native Kommunicate API, this operation is `POST /rest/ws/message/send` (base URL `https://services.kommunicate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-attachments.md) for the provider-specific parameters and requirements.

