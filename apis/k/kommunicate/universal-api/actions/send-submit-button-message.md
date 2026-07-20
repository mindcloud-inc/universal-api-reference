# Kommunicate: Send Submit Button Message

Creates a submit button message in Kommunicate.

```
POST https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/send-submit-button-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kommunicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/send-submit-button-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "message": "string",
  "fromUserName": "Ava Chen",
  "payloadJson": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/send-submit-button-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "message": "string",
    "fromUserName": "Ava Chen",
    "payloadJson": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | Conversation identifier to send the message into. |
| `message` | string | yes | Message text shown above the submit buttons. |
| `fromUserName` | string | yes | Sender user ID. |
| `payloadJson` | string<object> | yes | Array of submit button objects from the official template format. |
| `formData` | object | no | Key-value pairs submitted by the button action. |
| `formAction` | string | no | Destination URL for the submit action. |
| `requestType` | string | no | Submit encoding mode such as json. |

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

Through the native Kommunicate API, this operation is `POST /rest/ws/message/v2/send` (base URL `https://services.kommunicate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-submit-button-message.md) for the provider-specific parameters and requirements.

