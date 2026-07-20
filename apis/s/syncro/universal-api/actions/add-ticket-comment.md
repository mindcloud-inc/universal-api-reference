# Syncro: Add Ticket Comment

Adds a comment to a ticket in Syncro.

```
POST https://connect.mindcloud.co/v1/universal/syncro/latest/actions/add-ticket-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/add-ticket-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "subject": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/syncro/latest/actions/add-ticket-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "subject": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Syncro ticket ID. |
| `subject` | string | yes |  |
| `tech` | string | no |  |
| `body` | string | yes |  |
| `hidden` | boolean | no |  |
| `smsBody` | string | no |  |
| `doNotEmail` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": {
        "body": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "hidden": true,
        "id": 1,
        "subject": "string",
        "tech": "string",
        "ticketId": 1,
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "userId": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment.body` | string |  |
| `comment.createdAt` | date |  |
| `comment.hidden` | boolean |  |
| `comment.id` | number |  |
| `comment.subject` | string |  |
| `comment.tech` | string |  |
| `comment.ticketId` | number |  |
| `comment.updatedAt` | date |  |
| `comment.userId` | number |  |

## Native endpoint

Through the native Syncro API, this operation is `POST /tickets/:id/comment` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-ticket-comment.md) for the provider-specific parameters and requirements.

