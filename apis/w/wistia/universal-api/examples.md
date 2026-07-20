# Wistia Universal API Examples

These examples use the MindCloud API key and Wistia connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Account

Retrieves the current Wistia account details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wistia/latest/actions/get-current-account?${params}`, {
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
      "channelCount": 1,
      "folderCount": 1,
      "id": 1,
      "mediaCount": 1,
      "name": "Ava Chen",
      "url": "https://example.com",
      "videoLimit": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Current Account action reference](actions/get-current-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wistia/latest/actions/get-current-account).

## Archive Media

Archives one or more media items in Wistia.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/archive-media" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaHashedIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wistia/latest/actions/archive-media', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaHashedIds[]": ["string"]
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
      "backgroundJobStatus": {
        "id": 1,
        "status": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Archive Media action reference](actions/archive-media.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wistia/latest/actions/archive-media).
