# Peekalink Universal API Examples

These examples use the MindCloud API key and Peekalink connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get a Link Preview

Retrieves a link preview from Peekalink.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peekalink/latest/actions/get-link-preview?connectionId=$CONNECTION_ID&link=https%3A%2F%2Fwww.peekalink.io%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "link": "https://www.peekalink.io/"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peekalink/latest/actions/get-link-preview?${params}`, {
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
      "description": "string",
      "domain": "string",
      "icon": {},
      "id": 1,
      "image": {},
      "ok": true,
      "page": {},
      "redirected": true,
      "requestId": "string",
      "size": 1,
      "status": 1,
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get a Link Preview action reference](actions/get-link-preview.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/peekalink/latest/actions/get-link-preview).
