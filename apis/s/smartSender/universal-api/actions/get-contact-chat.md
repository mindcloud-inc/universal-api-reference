# Smart Sender: Get Contact Chat

Retrieves a contact's chat from Smart Sender.

```
GET https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/get-contact-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/get-contact-chat?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/get-contact-chat?${params}`, {
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
| `contactId` | string | yes | The Smart Sender contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canReply": true,
      "id": 1,
      "image": "string",
      "isClosed": true,
      "lastMessage": {},
      "phone": "string",
      "state": {},
      "timeAnswer": "2026-05-07T12:00:00.000Z",
      "timeClose": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "type": "string",
      "unreadMessages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canReply` | boolean |  |
| `id` | number |  |
| `image` | string |  |
| `isClosed` | boolean |  |
| `lastMessage` | object |  |
| `phone` | string |  |
| `state` | object |  |
| `timeAnswer` | date |  |
| `timeClose` | date |  |
| `title` | string |  |
| `type` | string |  |
| `unreadMessages` | number |  |

## Native endpoint

Through the native Smart Sender API, this operation is `GET /v1/contacts/:contactId/chat` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-chat.md) for the provider-specific parameters and requirements.

