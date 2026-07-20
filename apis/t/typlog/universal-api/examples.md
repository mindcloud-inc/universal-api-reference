# Typlog Universal API Examples

These examples use the MindCloud API key and Typlog connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sites

Retrieves sites from Typlog.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typlog/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typlog/latest/actions/list-sites?${params}`, {
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
      "baseUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "favicon": "string",
      "id": 1,
      "languages": [
        "string"
      ],
      "name": "Ava Chen",
      "primaryLang": "string",
      "slug": "string",
      "status": "string",
      "summary": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": "string",
      "zoneinfo": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Sites action reference](actions/list-sites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/typlog/latest/actions/list-sites).

## Create Episode

Creates a new episode in Typlog.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typlog/latest/actions/create-episode" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "4863",
  "title": "Episode One",
  "slug": "episode-one",
  "lang": "en",
  "format": "markdown"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typlog/latest/actions/create-episode', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "4863",
    "title": "Episode One",
    "slug": "episode-one",
    "lang": "en",
    "format": "markdown"
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
      "audio": {},
      "author": "string",
      "comment": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "episode": 1,
      "episodeType": "string",
      "explicit": true,
      "format": "string",
      "guests": [
        {}
      ],
      "hosts": [
        {}
      ],
      "id": 1,
      "image": "string",
      "lang": "string",
      "metadata": {},
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "season": 1,
      "slug": "string",
      "status": "string",
      "subtitle": "string",
      "tags": [
        {}
      ],
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Episode action reference](actions/create-episode.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/typlog/latest/actions/create-episode).
