# SendApp Universal API Examples

These examples use the MindCloud API key and SendApp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Templates



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendApp/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendApp/latest/actions/list-templates?${params}`, {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Templates action reference](actions/list-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendApp/latest/actions/list-templates).

## Send Media Message



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendApp/latest/actions/send-media-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaUrl": "https://example.com",
  "number": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendApp/latest/actions/send-media-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaUrl": "https://example.com",
    "number": "string",
    "type": "string"
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send Media Message action reference](actions/send-media-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendApp/latest/actions/send-media-message).
