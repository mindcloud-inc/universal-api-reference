# Joonto: Get SMS Details



```
GET https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-sms-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Joonto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-sms-details?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-sms-details?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callerName": "Ava Chen",
      "conversationId": 1,
      "dateCreated": "string",
      "direction": "string",
      "from": "string",
      "fromPretty": "string",
      "id": 1,
      "isAttachmentAudio": true,
      "isAttachmentImage": true,
      "isAttachmentUnsupported": true,
      "isAttachmentVideo": true,
      "mediaUrl": "https://example.com",
      "message": "string",
      "messageType": "string",
      "price": 1,
      "sentTime": "string",
      "sid": "string",
      "to": "string",
      "toPretty": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callerName` | string |  |
| `conversationId` | number |  |
| `dateCreated` | string |  |
| `direction` | string |  |
| `from` | string |  |
| `fromPretty` | string |  |
| `id` | number |  |
| `isAttachmentAudio` | boolean |  |
| `isAttachmentImage` | boolean |  |
| `isAttachmentUnsupported` | boolean |  |
| `isAttachmentVideo` | boolean |  |
| `mediaUrl` | string |  |
| `message` | string |  |
| `messageType` | string |  |
| `price` | number |  |
| `sentTime` | string |  |
| `sid` | string |  |
| `to` | string |  |
| `toPretty` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Joonto API, this operation is `GET /api/SMS/Get/:id` (base URL `https://api.joonto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-details.md) for the provider-specific parameters and requirements.

