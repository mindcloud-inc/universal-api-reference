# NeetoDesk: Create Draft Comment



```
POST https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/create-draft-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/create-draft-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/create-draft-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | string | yes | Identifier of the ticket. |
| `content` | string | yes | Content for the draft comment. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commentType` | string | no | Type of draft comment. |
| `authorEmail` | string | no | Email of the person creating the draft. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NeetoDesk API returns.

## Native endpoint

Through the native NeetoDesk API, this operation is `POST /tickets/:ticket_id/drafts` (base URL `https://{{credentials.workspaceSubdomain}}.neetodesk.com/api/external/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft-comment.md) for the provider-specific parameters and requirements.

