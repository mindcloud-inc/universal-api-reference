# BulkSMS Universal API Examples

These examples use the MindCloud API key and BulkSMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile

Retrieves your account profile from BulkSMS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/get-profile?${params}`, {
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
      "commerce": {},
      "company": {},
      "created": "2026-05-07T12:00:00.000Z",
      "credits": {},
      "id": "string",
      "originAddresses": {},
      "quota": {},
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Profile action reference](actions/get-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bulkSMS/latest/actions/get-profile).

## Create Attachment Upload URL

Creates a signed BulkSMS attachment upload URL.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/create-attachment-upload-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileExtension": "string",
  "mediaType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/create-attachment-upload-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileExtension": "string",
    "mediaType": "string"
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
      "fetchUrl": "https://example.com",
      "fields": [
        {}
      ],
      "putUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Attachment Upload URL action reference](actions/create-attachment-upload-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bulkSMS/latest/actions/create-attachment-upload-url).
