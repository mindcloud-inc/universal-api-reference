# Vimeo Universal API Examples

These examples use the MindCloud API key and Vimeo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Channel

Retrieves a channel record from Vimeo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-channel?connectionId=$CONNECTION_ID&channelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-channel?${params}`, {
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
        {}
      ],
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "header": {},
      "link": "https://example.com",
      "metadata": {},
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "pictures": {},
      "privacy": {},
      "resourceKey": "string",
      "tags": [
        {}
      ],
      "uri": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Channel action reference](actions/get-channel.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vimeo/latest/actions/get-channel).

## Add Video to Project

Adds a video to a project in Vimeo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/add-video-to-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "152184",
  "projectId": "12345",
  "videoId": "33031367"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/add-video-to-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "152184",
    "projectId": "12345",
    "videoId": "33031367"
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Video to Project action reference](actions/add-video-to-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vimeo/latest/actions/add-video-to-project).
