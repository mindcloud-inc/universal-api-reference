# HelpSpace: Create Ticket Message

Creates a ticket message in HelpSpace.

```
POST https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/create-ticket-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/create-ticket-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/create-ticket-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | string | yes | HelpSpace ticket identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "bcc": [
        "string"
      ],
      "body": "string",
      "cc": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fromContact": {},
      "id": 1,
      "inlineImages": [
        {}
      ],
      "subject": "string",
      "to": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `bcc` | array<string> |  |
| `body` | string |  |
| `cc` | array<string> |  |
| `createdAt` | date |  |
| `fromContact` | object |  |
| `id` | number |  |
| `inlineImages` | array<object> |  |
| `subject` | string |  |
| `to` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native HelpSpace API, this operation is `POST /tickets/{id}/messages` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket-message.md) for the provider-specific parameters and requirements.

