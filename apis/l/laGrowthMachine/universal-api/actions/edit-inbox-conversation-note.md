# LaGrowthMachine: Edit Inbox Conversation Note

Updates an inbox conversation note in LaGrowthMachine.

```
PUT https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/edit-inbox-conversation-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaGrowthMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/edit-inbox-conversation-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/edit-inbox-conversation-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "note": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | no | Optional campaign filter when resolving the conversation. |
| `campaignName` | string | no | Optional campaign-name filter when resolving the conversation. |
| `conversationId` | string | no | Conversation ID. Fastest and most reliable identifier when available. |
| `email` | string | no | Lead email used to resolve the conversation. |
| `identityId` | string | no | Optional identity filter when resolving the conversation. |
| `leadId` | string | no | Lead ID used to resolve the conversation. |
| `linkedinUrl` | string | no | Lead LinkedIn URL used to resolve the conversation. |
| `mode` | string | no | Either `replace` or `append`. |
| `note` | string | yes | Note content to store on the conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "conversationId": "string",
        "leadId": "string",
        "mode": "string",
        "note": "string",
        "noteLength": 1,
        "timestamp": "string",
        "truncated": true
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.conversationId` | string | Conversation identifier. |
| `data.leadId` | string | Lead identifier. |
| `data.mode` | string | How the note update was applied. |
| `data.note` | string | Full conversation note content after the edit. |
| `data.noteLength` | number | Length of the resulting note. |
| `data.timestamp` | string | Timestamp of the note update. |
| `data.truncated` | boolean | Whether the provider truncated the note content. |
| `success` | boolean | Whether the conversation note edit request succeeded. |

## Native endpoint

Through the native LaGrowthMachine API, this operation is `POST /inbox/conversations/note` (base URL `https://apiv2.lagrowthmachine.com/flow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-inbox-conversation-note.md) for the provider-specific parameters and requirements.

