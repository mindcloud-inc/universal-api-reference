# NeetoDesk: Create Ticket



```
POST https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "subject": "string",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "subject": "string",
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address of the customer. |
| `subject` | string | yes | Subject for the ticket. |
| `description` | string | yes | Description for the ticket. |
| `name` | string | no | Name of the customer. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel` | string | no | Source of the ticket. |
| `assigneeEmail` | string | no | Email address belonging to a team member. |
| `status` | string | no | Status for the ticket. |
| `priority` | string | no | Priority for the ticket. |
| `category` | string | no | Category for the ticket. |
| `tags[]` | array<string> | no | Tags to assign to the ticket. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ticket": {
        "id": "string",
        "number": 1,
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ticket.id` | string | Unique identifier for the created ticket. |
| `ticket.number` | number | Display number for the created ticket. |
| `ticket.url` | string | Admin URL for the created ticket. |

## Native endpoint

Through the native NeetoDesk API, this operation is `POST /tickets` (base URL `https://{{credentials.workspaceSubdomain}}.neetodesk.com/api/external/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

