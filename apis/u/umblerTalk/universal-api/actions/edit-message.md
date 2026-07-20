# Umbler Talk: Edit Message

Updates an existing message in Umbler Talk.

```
PUT https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/edit-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/edit-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "newMessage": "string",
  "organizationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/edit-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "newMessage": "string",
    "organizationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The message ID. |
| `newMessage` | string | yes | Updated message text. |
| `organizationId` | string | yes | The organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_t": "string",
      "chat": {},
      "contactId": "string",
      "contacts": [
        {}
      ],
      "content": "string",
      "createdAtUTC": "2026-05-07T12:00:00.000Z",
      "eventAtUTC": "2026-05-07T12:00:00.000Z",
      "file": {},
      "fromContact": {},
      "id": "string",
      "isPrivate": true,
      "messageState": "string",
      "messageType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_t` | string |  |
| `chat` | object |  |
| `contactId` | string |  |
| `contacts` | array<object> |  |
| `content` | string |  |
| `createdAtUTC` | date |  |
| `eventAtUTC` | date |  |
| `file` | object |  |
| `fromContact` | object |  |
| `id` | string |  |
| `isPrivate` | boolean |  |
| `messageState` | string |  |
| `messageType` | string |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `PUT /v1/messages/[:id]/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-message.md) for the provider-specific parameters and requirements.

