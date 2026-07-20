# Chat Aid Universal API Examples

These examples use the MindCloud API key and Chat Aid connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Submit Question

Submits a question to Chat Aid for asynchronous completion.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/submit-question?connectionId=$CONNECTION_ID&prompt=What%20is%20our%20refund%20policy%3F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "prompt": "What is our refund policy?"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/submit-question?${params}`, {
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
      "ok": true,
      "pollEndpoint": "string",
      "promptId": "string",
      "timeInterval": 1,
      "votingEndpoint": "string"
    }
  ],
  "meta": {}
}
```

See the full [Submit Question action reference](actions/submit-question.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatAid/latest/actions/submit-question).

## Upload Custom Sources

Uploads new custom sources to Chat Aid.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/upload-custom-sources" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/upload-custom-sources', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files": "string"
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
      "message": "string",
      "ok": true
    }
  ],
  "meta": {}
}
```

See the full [Upload Custom Sources action reference](actions/upload-custom-sources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatAid/latest/actions/upload-custom-sources).
