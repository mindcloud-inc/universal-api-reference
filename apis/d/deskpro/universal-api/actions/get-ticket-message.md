# Deskpro: Get Ticket Message

Retrieves a ticket message from Deskpro.

```
GET https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-ticket-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deskpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-ticket-message?connectionId=$CONNECTION_ID&ticketId=3&messageId=3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "3",
  "messageId": "3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-ticket-message?${params}`, {
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
| `ticketId` | number | yes | The Deskpro ticket id containing the message. Example: `3`. |
| `messageId` | number | yes | The Deskpro ticket message id to retrieve. Example: `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": [
        {
          "dateCreated": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "type": "string",
          "value": "string"
        }
      ],
      "creationSystem": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailSource": 1,
      "hostname": "Ava Chen",
      "id": 1,
      "ipAddress": "string",
      "isAgentNote": true,
      "langCode": "string",
      "message": "string",
      "messageFull": "string",
      "messageHash": "string",
      "messagePreviewText": "string",
      "messageRaw": "string",
      "messageWithoutImages": "string",
      "person": 1,
      "showFullHint": true,
      "ticket": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes[].dateCreated` | date |  |
| `attributes[].name` | string |  |
| `attributes[].type` | string |  |
| `attributes[].value` | string |  |
| `creationSystem` | string |  |
| `dateCreated` | date |  |
| `email` | string |  |
| `emailSource` | number |  |
| `hostname` | string |  |
| `id` | number |  |
| `ipAddress` | string |  |
| `isAgentNote` | boolean |  |
| `langCode` | string |  |
| `message` | string |  |
| `messageFull` | string |  |
| `messageHash` | string |  |
| `messagePreviewText` | string |  |
| `messageRaw` | string |  |
| `messageWithoutImages` | string |  |
| `person` | number |  |
| `showFullHint` | boolean |  |
| `ticket` | number |  |

## Native endpoint

Through the native Deskpro API, this operation is `GET /tickets/:ticketId/messages/:messageId` (base URL `{{credentials.helpdeskUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-message.md) for the provider-specific parameters and requirements.

