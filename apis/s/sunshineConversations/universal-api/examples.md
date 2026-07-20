# Sunshine Conversations Universal API Examples

These examples use the MindCloud API key and Sunshine Conversations connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Integrations

Retrieves configured integrations from Sunshine Conversations.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/list-integrations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/list-integrations?${params}`, {
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
  "data": [
    {
      "integrations": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

See the full [List Integrations action reference](actions/list-integrations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sunshineConversations/latest/actions/list-integrations).

## Create Conversation

Creates a new conversation in Sunshine Conversations.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/create-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/create-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "conversation": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Conversation action reference](actions/create-conversation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sunshineConversations/latest/actions/create-conversation).
