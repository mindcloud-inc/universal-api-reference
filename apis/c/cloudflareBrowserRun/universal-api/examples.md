# Cloudflare Browser Run Universal API Examples

These examples use the MindCloud API key and Cloudflare Browser Run connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify API Token

Verifies whether a Cloudflare API token works.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/verify-api-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/verify-api-token?${params}`, {
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
      "errors": [
        {}
      ],
      "messages": [
        {}
      ],
      "result": {
        "expires_on": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "status": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Verify API Token action reference](actions/verify-api-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudflareBrowserRun/latest/actions/verify-api-token).

## Activate Browser Target

Activates a browser target in Cloudflare Browser Run.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/activate-browser-target" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string",
  "targetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/activate-browser-target', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string",
    "targetId": "string"
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Activate Browser Target action reference](actions/activate-browser-target.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudflareBrowserRun/latest/actions/activate-browser-target).
