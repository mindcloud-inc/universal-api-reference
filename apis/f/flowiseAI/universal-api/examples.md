# FlowiseAI Universal API Examples

These examples use the MindCloud API key and FlowiseAI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Chatflows

Retrieves a list of chatflows from FlowiseAI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-chatflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/list-chatflows?${params}`, {
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
      "analytic": "string",
      "apiConfig": "string",
      "apikeyid": "string",
      "category": "string",
      "chatbotConfig": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "deployed": true,
      "flowData": "string",
      "id": "string",
      "isPublic": true,
      "name": "Ava Chen",
      "speechToText": "string",
      "type": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Chatflows action reference](actions/list-chatflows.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flowiseAI/latest/actions/list-chatflows).

## Create Attachment Array

Creates an attachment array for a FlowiseAI chat.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/create-attachment-array" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatflowId": "string",
  "chatId": "string",
  "files[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/create-attachment-array', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatflowId": "string",
    "chatId": "string",
    "files[]": ["string"]
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
      "content": "string",
      "mimeType": "string",
      "name": "Ava Chen",
      "size": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Attachment Array action reference](actions/create-attachment-array.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flowiseAI/latest/actions/create-attachment-array).
