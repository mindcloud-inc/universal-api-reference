# Hippo Video Universal API Examples

These examples use the MindCloud API key and Hippo Video connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Video Categories

Retrieves video categories from Hippo Video.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/list-video-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/list-video-categories?${params}`, {
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
        [
          {}
        ]
      ],
      "code": 1
    }
  ],
  "meta": {}
}
```

See the full [List Video Categories action reference](actions/list-video-categories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hippoVideo/latest/actions/list-video-categories).

## Generate Bulk Personalized Video Tracking IDs

Creates bulk personalized video tracking IDs in Hippo Video.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/generate-bulk-personalized-video-tracking-ids" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoId": 1,
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/generate-bulk-personalized-video-tracking-ids', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoId": 1,
    "file": "string"
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
      "code": 1,
      "msg": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate Bulk Personalized Video Tracking IDs action reference](actions/generate-bulk-personalized-video-tracking-ids.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hippoVideo/latest/actions/generate-bulk-personalized-video-tracking-ids).
