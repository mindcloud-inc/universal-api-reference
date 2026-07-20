# Voiceflow Universal API Examples

These examples use the MindCloud API key and Voiceflow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Conversation State

Retrieves a user's conversation state from Voiceflow.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-conversation-state?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-conversation-state?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Get Conversation State action reference](actions/get-conversation-state.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voiceflow/latest/actions/get-conversation-state).

## Create Document

Creates a knowledge base document in Voiceflow.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": "[object Object]"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Document action reference](actions/create-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voiceflow/latest/actions/create-document).
