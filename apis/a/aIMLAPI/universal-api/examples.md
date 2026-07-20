# AI/ML API Universal API Examples

These examples use the MindCloud API key and AI/ML API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Balance

Retrieves the account balance from AI/ML API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/get-account-balance?${params}`, {
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

See the full [Get Account Balance action reference](actions/get-account-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aIMLAPI/latest/actions/get-account-balance).

## Create Claude 3.5 Haiku Chat Completion



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/create-claude35-haiku-chat-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/create-claude35-haiku-chat-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[]": [{}]
  })
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

See the full [Create Claude 3.5 Haiku Chat Completion action reference](actions/create-claude35-haiku-chat-completion.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aIMLAPI/latest/actions/create-claude35-haiku-chat-completion).
