# Atera: Add ticket comment

Creates a comment on a specific Atera ticket.

```
POST https://connect.mindcloud.co/v1/universal/atera/latest/actions/add-ticket-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atera/latest/actions/add-ticket-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": 1,
  "commentText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atera/latest/actions/add-ticket-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": 1,
    "commentText": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commentTimestampUtc` | string | no | UTC comment timestamp. |
| `enduserCommentDetails.enduserId` | number | no | End user ID for end user comments. |
| `technicianCommentDetails.isInternal` | boolean | no | Whether the technician comment is internal. |
| `technicianCommentDetails.technicianEmail` | string | no | Technician email for technician comments. |
| `technicianCommentDetails.technicianId` | number | no | Technician ID for technician comments. |
| `ticketId` | number | yes | System ticket ID. |
| `commentText` | string | yes | Comment text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActionID` | string |  |

## Native endpoint

Through the native Atera API, this operation is `POST /api/v3/tickets/:ticketId/comments` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-ticket-comment.md) for the provider-specific parameters and requirements.

