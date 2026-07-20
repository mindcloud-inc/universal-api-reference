# ChatPDF Universal API Examples

These examples use the MindCloud API key and ChatPDF connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Send Chat Message



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/send-chat-message?connectionId=$CONNECTION_ID&sourceId=src_xxxxxx&messages%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceId": "src_xxxxxx",
  "messages[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/send-chat-message?${params}`, {
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
      "content": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send Chat Message action reference](actions/send-chat-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatPDF/latest/actions/send-chat-message).

## Add PDF From URL



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/add-pdf-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/file.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/add-pdf-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/file.pdf"
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
      "sourceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add PDF From URL action reference](actions/add-pdf-from-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatPDF/latest/actions/add-pdf-from-url).
