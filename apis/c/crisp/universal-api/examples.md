# Crisp Universal API Examples

These examples use the MindCloud API key and Crisp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Plugin Account

Retrieves your plugin account from Crisp.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-plugin-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-plugin-account?${params}`, {
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
      "pluginId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Plugin Account action reference](actions/get-plugin-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crisp/latest/actions/get-plugin-account).

## Create New Conversation

Creates a new conversation in Crisp.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crisp/latest/actions/create-new-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "websiteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crisp/latest/actions/create-new-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "websiteId": "string"
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
      "sessionId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create New Conversation action reference](actions/create-new-conversation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crisp/latest/actions/create-new-conversation).
