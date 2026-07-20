# ChipBot Universal API Examples

These examples use the MindCloud API key and ChipBot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Connect Domain



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/connect-domain?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/connect-domain?${params}`, {
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
      "data": {
        "accountId": "string",
        "apiKey": "string",
        "domainId": "string",
        "domainName": "Ava Chen",
        "expiresIn": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "token": "string",
        "type": "string"
      },
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Connect Domain action reference](actions/connect-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chipBot/latest/actions/connect-domain).

## Reply to Message



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/reply-to-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/reply-to-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "message": "string"
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
      "data": {},
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Reply to Message action reference](actions/reply-to-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chipBot/latest/actions/reply-to-message).
