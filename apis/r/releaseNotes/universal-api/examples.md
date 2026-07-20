# ReleaseNotes Universal API Examples

These examples use the MindCloud API key and ReleaseNotes connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Latest Release

Retrieves the latest release from ReleaseNotes.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/get-latest-release?connectionId=$CONNECTION_ID&projectId=11233" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "11233"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/get-latest-release?${params}`, {
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
      "description": "string",
      "externalId": "string",
      "featuredImage": "string",
      "featuredImageUrl": "https://example.com",
      "id": "string",
      "involved": [
        {
          "avatar": "string",
          "name": "Ava Chen"
        }
      ],
      "owner": {
        "avatar": "string",
        "name": "Ava Chen"
      },
      "private": true,
      "releasedAt": 1,
      "releasedAtHuman": "string",
      "socialImage": "string",
      "status": "string",
      "title": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Latest Release action reference](actions/get-latest-release.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/releaseNotes/latest/actions/get-latest-release).

## Add to Notes Feed

Creates a new notes feed item in ReleaseNotes.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/add-to-notes-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "11233",
  "notes": "Released a small dashboard performance improvement and filter fix."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/add-to-notes-feed', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "11233",
    "notes": "Released a small dashboard performance improvement and filter fix."
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
      "note": {
        "attribution": "string",
        "createdAt": "string",
        "description": "string",
        "externalId": "string",
        "externalLink": "https://example.com",
        "id": 1,
        "noteAsHtml": "string",
        "noteAsText": "string",
        "source": "string",
        "teamId": 1,
        "title": "string",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Add to Notes Feed action reference](actions/add-to-notes-feed.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/releaseNotes/latest/actions/add-to-notes-feed).
