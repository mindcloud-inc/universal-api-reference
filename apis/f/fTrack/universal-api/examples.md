# FTrack Universal API Examples

These examples use the MindCloud API key and FTrack connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Query Server Information

Retrieves server information from FTrack.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/query-server-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/query-server-information?${params}`, {
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

See the full [Query Server Information action reference](actions/query-server-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fTrack/latest/actions/query-server-information).

## Complete Multipart Upload

Completes a multipart upload in FTrack.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/complete-multipart-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "componentId": "string",
  "uploadId": "string",
  "parts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/complete-multipart-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "componentId": "string",
    "uploadId": "string",
    "parts[]": [{}]
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

See the full [Complete Multipart Upload action reference](actions/complete-multipart-upload.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fTrack/latest/actions/complete-multipart-upload).
