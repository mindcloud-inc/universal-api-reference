# Upload to URL Universal API Examples

These examples use the MindCloud API key and Upload to URL connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get File Information



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uploadToURL/latest/actions/get-file-information?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadToURL/latest/actions/get-file-information?${params}`, {
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
      "expires_at": "2026-05-07T12:00:00.000Z",
      "file_size": 1,
      "filename": "Ava Chen",
      "id": "string",
      "is_expired": true,
      "mime_type": "string",
      "public_url": "https://example.com",
      "retention_days": 1,
      "uploaded_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get File Information action reference](actions/get-file-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uploadToURL/latest/actions/get-file-information).

## Publish HTML



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uploadToURL/latest/actions/publish-html" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "htmlCode": "string",
  "pagePath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uploadToURL/latest/actions/publish-html', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "htmlCode": "string",
    "pagePath": "string"
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
      "credits_remaining": 1,
      "message": "string",
      "page_path": "string",
      "pretty_url": "https://example.com",
      "status": "string",
      "subdomain": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Publish HTML action reference](actions/publish-html.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uploadToURL/latest/actions/publish-html).
