# Moxie: Create Comment on Ticket

Creates a comment on a ticket in Moxie.

```
POST https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-comment-on-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-comment-on-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userEmail": "ava@example.com",
  "ticketNumber": 1,
  "privateComment": true,
  "comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-comment-on-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userEmail": "ava@example.com",
    "ticketNumber": 1,
    "privateComment": true,
    "comment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userEmail` | string | yes | Email of the user posting the comment. |
| `ticketNumber` | number | yes | Numeric ticket number. |
| `privateComment` | boolean | yes | Whether the comment is private. |
| `comment` | string | yes | Comment body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {}
      ],
      "ticket": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | array<object> |  |
| `ticket` | object |  |

## Native endpoint

Through the native Moxie API, this operation is `POST /action/tickets/comments/create` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment-on-ticket.md) for the provider-specific parameters and requirements.

