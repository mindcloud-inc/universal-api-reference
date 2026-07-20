# ZapCap Universal API Examples

These examples use the MindCloud API key and ZapCap connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Templates

Retrieves available templates from ZapCap.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/list-templates?${params}`, {
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
      "categories": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "previews": {
        "previewGif": "string",
        "previewMp4": "string"
      },
      "previewUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Templates action reference](actions/list-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zapCap/latest/actions/list-templates).

## Approve Transcript

Approves a transcript for a ZapCap task.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/approve-transcript" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/approve-transcript', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoId": "string",
    "id": "string"
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

See the full [Approve Transcript action reference](actions/approve-transcript.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zapCap/latest/actions/approve-transcript).
