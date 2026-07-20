# 2Chat: Get Messages by Phone Number

Retrieves WhatsApp messages in 2Chat by phone number.

```
GET https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-messages-by-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-messages-by-phone-number?connectionId=$CONNECTION_ID&from_number=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from_number": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-messages-by-phone-number?${params}`, {
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
| `from_number` | string | yes | The WhatsApp number connected to 2Chat whose messages you want to fetch. |
| `remote_number` | string | no | Optional remote WhatsApp number to scope messages to one conversation. |
| `pageNumber` | number | no | Zero-based page number for older message pages. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messages": [
        {
          "channelPhoneNumber": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "message": {
            "text": {}
          },
          "read": true,
          "received": true,
          "remotePhoneNumber": "string",
          "sent": true,
          "sentBy": "string",
          "sessionKey": "string",
          "uuid": "string"
        }
      ],
      "pageNumber": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messages[].channelPhoneNumber` | string |  |
| `messages[].createdAt` | date |  |
| `messages[].id` | string |  |
| `messages[].message.text` | object |  |
| `messages[].read` | boolean |  |
| `messages[].received` | boolean |  |
| `messages[].remotePhoneNumber` | string |  |
| `messages[].sent` | boolean |  |
| `messages[].sentBy` | string |  |
| `messages[].sessionKey` | string |  |
| `messages[].uuid` | string |  |
| `pageNumber` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native 2Chat API, this operation is `GET /whatsapp/messages/:from_number/:remote_number` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-messages-by-phone-number.md) for the provider-specific parameters and requirements.

