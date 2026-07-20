# RemasterMedia Universal API Examples

These examples use the MindCloud API key and RemasterMedia connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Mediafile

Retrieves mediafile details from RemasterMedia.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/get-mediafile?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/get-mediafile?${params}`, {
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
      "mediafile": {
        "action": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "expires_at": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "metadata": {},
        "options": {},
        "status": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "url": "https://example.com",
        "user_data": {},
        "webhook_url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Mediafile action reference](actions/get-mediafile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/remasterMedia/latest/actions/get-mediafile).

## Authenticate

Creates an auth token in RemasterMedia.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/authenticate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/authenticate', {
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
      "expiration": "2026-05-07T12:00:00.000Z",
      "token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Authenticate action reference](actions/authenticate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/remasterMedia/latest/actions/authenticate).
