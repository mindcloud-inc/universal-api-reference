# leadtributor.cloud Universal API Examples

These examples use the MindCloud API key and leadtributor.cloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test API Access

Retrieves an API access test result from leadtributor.cloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/test-api-access?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/test-api-access?${params}`, {
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
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test API Access action reference](actions/test-api-access.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leadtributorcloud/latest/actions/test-api-access).

## Announce Lead Attachment Upload

Creates an attachment upload request for a lead in leadtributor.cloud.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/announce-lead-attachment-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contentType": "string",
  "filename": "Ava Chen",
  "leadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/announce-lead-attachment-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contentType": "string",
    "filename": "Ava Chen",
    "leadId": "string"
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
      "fields": {},
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Announce Lead Attachment Upload action reference](actions/announce-lead-attachment-upload.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leadtributorcloud/latest/actions/announce-lead-attachment-upload).
