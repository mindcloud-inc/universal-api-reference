# Joonto: Get SMS By User And Phone Number



```
GET https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-sms-by-user-and-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Joonto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-sms-by-user-and-phone-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-sms-by-user-and-phone-number?${params}`, {
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
| `phone` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachment": {
        "mmsType": "string",
        "mmsUrl": "https://example.com"
      },
      "callerName": "Ava Chen",
      "conversationId": 1,
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "direction": "string",
      "from": "string",
      "fromEmail": "ava@example.com",
      "fromImageId": 1,
      "fromName": "Ava Chen",
      "fromPretty": "string",
      "groupNumbers": "string",
      "id": 1,
      "isAttachmentAudio": true,
      "isAttachmentImage": true,
      "isAttachmentUnsupported": true,
      "isAttachmentVideo": true,
      "mediaType": "string",
      "mediaUrl": "https://example.com",
      "message": "string",
      "messageType": "string",
      "originalFrom": "string",
      "originalTo": "string",
      "price": 1,
      "sentTime": "2026-05-07T12:00:00.000Z",
      "sid": "string",
      "to": "string",
      "toEmail": "ava@example.com",
      "toImageId": 1,
      "toName": "Ava Chen",
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
| `attachment.mmsType` | string |  |
| `attachment.mmsUrl` | string |  |
| `callerName` | string |  |
| `conversationId` | number |  |
| `dateCreated` | date |  |
| `direction` | string |  |
| `from` | string |  |
| `fromEmail` | string |  |
| `fromImageId` | number |  |
| `fromName` | string |  |
| `fromPretty` | string |  |
| `groupNumbers` | string |  |
| `id` | number |  |
| `isAttachmentAudio` | boolean |  |
| `isAttachmentImage` | boolean |  |
| `isAttachmentUnsupported` | boolean |  |
| `isAttachmentVideo` | boolean |  |
| `mediaType` | string |  |
| `mediaUrl` | string |  |
| `message` | string |  |
| `messageType` | string |  |
| `originalFrom` | string |  |
| `originalTo` | string |  |
| `price` | number |  |
| `sentTime` | date |  |
| `sid` | string |  |
| `to` | string |  |
| `toEmail` | string |  |
| `toImageId` | number |  |
| `toName` | string |  |
| `toPretty` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Joonto API, this operation is `GET /api/SMS/GetByUserAndPhoneNumber` (base URL `https://api.joonto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-by-user-and-phone-number.md) for the provider-specific parameters and requirements.

