# Request Tracker (RT): Create Ticket

Creates a new ticket in Request Tracker.

```
POST https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Request Tracker (RT) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "queue": "string",
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "queue": "string",
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `adminCc` | string | no | Admin Cc email address or RT user name. |
| `cc` | string | no | Cc email address or RT user name. |
| `content` | string | no | Initial ticket content or description. |
| `owner` | string | no | Owner user ID or username for the ticket. |
| `priority` | number | no | Initial RT ticket priority value. |
| `queue` | string | yes | Queue name or ID for the new ticket. |
| `requestor` | string | no | Requestor email address or RT user name. |
| `status` | string | no | Initial RT ticket status. |
| `subject` | string | yes | Subject line for the new ticket. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentType` | string | no | Content type for the initial ticket content, for example text/plain or text/html. Default: `text/plain`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "type": "string",
      "Url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `type` | string |  |
| `Url` | string |  |

## Native endpoint

Through the native Request Tracker (RT) API, this operation is `POST ticket` (base URL `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

