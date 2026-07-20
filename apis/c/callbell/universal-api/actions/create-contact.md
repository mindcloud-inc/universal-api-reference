# Callbell: Create Contact

Creates a new contact in Callbell.

```
POST https://connect.mindcloud.co/v1/universal/callbell/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callbell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callbell/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string",
  "name": "Ava Chen",
  "source": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callbell/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string",
    "name": "Ava Chen",
    "source": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignedUser` | string | no | Collaborator email to assign to the contact. |
| `botStatus` | string | no | Bot status to apply to the contact. |
| `channelUuid` | string | no | Channel UUID to associate with the contact. |
| `customFields` | object | no | Custom field values keyed by field name. |
| `identifier` | string | yes | Phone number or platform identifier for the contact. |
| `name` | string | yes | Display name for the contact. |
| `source` | string | yes | Source of the contact, such as whatsapp. |
| `tags[]` | array<string> | no | List of existing Callbell tags to assign. |
| `teamUuid` | string | no | Team UUID to assign to the contact. |

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

Through the native Callbell API, this operation is `POST /contacts` (base URL `https://api.callbell.eu/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

