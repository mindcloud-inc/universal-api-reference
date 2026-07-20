# Noor Universal API Examples

These examples use the MindCloud API key and Noor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Space Members

Retrieves members for a Noor space.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noor/latest/actions/list-space-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noor/latest/actions/list-space-members?${params}`, {
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

See the full [List Space Members action reference](actions/list-space-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/noor/latest/actions/list-space-members).

## Send Message

Creates a message in a Noor thread.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/noor/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "thread": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/noor/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "thread": "string",
    "text": "string"
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

See the full [Send Message action reference](actions/send-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/noor/latest/actions/send-message).
