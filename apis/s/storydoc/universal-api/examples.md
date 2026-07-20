# Storydoc Universal API Examples

These examples use the MindCloud API key and Storydoc connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Details

Retrieves account details from Storydoc.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storydoc/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storydoc/latest/actions/get-account-details?${params}`, {
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
      "orgId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Details action reference](actions/get-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/storydoc/latest/actions/get-account-details).

## Create Story Version

Creates a new story version in Storydoc.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/storydoc/latest/actions/create-story-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "storyId": "string",
  "senderEmail": "ava@example.com",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/storydoc/latest/actions/create-story-version', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "storyId": "string",
    "senderEmail": "ava@example.com",
    "data": {}
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
      "editorUrl": "https://example.com",
      "shortUrl": "https://example.com",
      "url": "https://example.com",
      "versionId": "string",
      "versionUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Story Version action reference](actions/create-story-version.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/storydoc/latest/actions/create-story-version).
