# ImageKit.io Universal API Examples

These examples use the MindCloud API key and ImageKit.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List and Search Assets

Finds files in ImageKit.io with search and filter options.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/list-and-search-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/list-and-search-assets?${params}`, {
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
      "aiTags": [
        "string"
      ],
      "bitRate": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customCoordinates": {},
      "customMetadata": {},
      "duration": 1,
      "embeddedMetadata": {},
      "fileId": "string",
      "filePath": "string",
      "fileType": "string",
      "hasAlpha": true,
      "height": 1,
      "isPrivateFile": true,
      "isPublished": true,
      "mime": "string",
      "name": "Ava Chen",
      "size": 1,
      "tags": [
        "string"
      ],
      "thumbnail": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "versionInfo": {},
      "videoCodec": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

See the full [List and Search Assets action reference](actions/list-and-search-assets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/imageKit/latest/actions/list-and-search-assets).

## Add Tags Bulk

Adds tags to multiple files in ImageKit.io.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/add-tags-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/add-tags-bulk', {
  method: 'PUT',
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
      "successfullyUpdatedFileIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Tags Bulk action reference](actions/add-tags-bulk.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/imageKit/latest/actions/add-tags-bulk).
