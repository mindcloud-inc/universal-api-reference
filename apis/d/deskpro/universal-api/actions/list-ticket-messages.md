# Deskpro: List Ticket Messages

Retrieves a list of ticket messages from Deskpro.

```
GET https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-ticket-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deskpro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-ticket-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&ticketId=3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "ticketId": "3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-ticket-messages?${params}`, {
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
| `ticketId` | number | yes | The Deskpro ticket id whose messages to list. Example: `3`. |

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

Through the native Deskpro API, this operation is `GET /tickets/:ticketId/messages` (base URL `{{credentials.helpdeskUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ticket-messages.md) for the provider-specific parameters and requirements.

