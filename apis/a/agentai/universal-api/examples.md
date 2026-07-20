# Agent.ai Universal API Examples

These examples use the MindCloud API key and Agent.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Web Page Content

Retrieves web page text from Agent.ai by URL or domain.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-web-page-content?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-web-page-content?${params}`, {
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
      "metadata": {},
      "response": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Web Page Content action reference](actions/get-web-page-content.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agentai/latest/actions/get-web-page-content).

## Convert Text To Speech

Creates a speech audio file from text in Agent.ai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/convert-text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "textToSpeech": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentai/latest/actions/convert-text-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "textToSpeech": "string"
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
      "response": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Convert Text To Speech action reference](actions/convert-text-to-speech.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agentai/latest/actions/convert-text-to-speech).
