# Callbell: Open Contact Conversation

Reopens a contact conversation in Callbell.

```
PUT https://connect.mindcloud.co/v1/universal/callbell/latest/actions/open-contact-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callbell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callbell/latest/actions/open-contact-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callbell/latest/actions/open-contact-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | Unique identifier of the contact whose conversation should be opened. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedUser": {},
      "avatarUrl": "https://example.com",
      "blockedAt": "string",
      "channel": {},
      "closedAt": "string",
      "conversationHref": "string",
      "createdAt": "string",
      "customFields": {},
      "funnelId": "string",
      "href": "string",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "source": "string",
      "tags": [
        "string"
      ],
      "team": {},
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedUser` | object |  |
| `avatarUrl` | string |  |
| `blockedAt` | string |  |
| `channel` | object |  |
| `closedAt` | string |  |
| `conversationHref` | string |  |
| `createdAt` | string |  |
| `customFields` | object |  |
| `funnelId` | string |  |
| `href` | string |  |
| `name` | string |  |
| `phoneNumber` | string |  |
| `source` | string |  |
| `tags` | array<string> |  |
| `team` | object |  |
| `uuid` | string |  |

## Native endpoint

Through the native Callbell API, this operation is `POST /contacts/:uuid/conversation/open` (base URL `https://api.callbell.eu/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/open-contact-conversation.md) for the provider-specific parameters and requirements.

