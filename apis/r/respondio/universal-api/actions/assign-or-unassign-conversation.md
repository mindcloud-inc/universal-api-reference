# respond.io: Assign Or Unassign Conversation

Updates a conversation assignee in respond.io.

```
PUT https://connect.mindcloud.co/v1/universal/respondio/latest/actions/assign-or-unassign-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a respond.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/assign-or-unassign-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assignee": "string",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/respondio/latest/actions/assign-or-unassign-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assignee": "string",
    "identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignee` | string | yes | Assignee user identifier or null to unassign. |
| `identifier` | string | yes | Contact identifier (id:, email:, or phone:). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number |  |

## Native endpoint

Through the native respond.io API, this operation is `POST /contact/:identifier/conversation/assignee` (base URL `https://api.respond.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-or-unassign-conversation.md) for the provider-specific parameters and requirements.

