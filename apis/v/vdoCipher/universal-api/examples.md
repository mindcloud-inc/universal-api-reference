# VdoCipher Universal API Examples

These examples use the MindCloud API key and VdoCipher connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Videos

Lists videos in VdoCipher.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/list-videos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/list-videos?${params}`, {
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
      "count": 1,
      "rows": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Videos action reference](actions/list-videos.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vdoCipher/latest/actions/list-videos).

## Add Video Tags

Adds tags to videos in VdoCipher.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/add-video-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/add-video-tags', {
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
  "data": [],
  "meta": {}
}
```

See the full [Add Video Tags action reference](actions/add-video-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vdoCipher/latest/actions/add-video-tags).
