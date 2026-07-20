# Hex Universal API Examples

These examples use the MindCloud API key and Hex connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hex/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hex/latest/actions/list-projects?${params}`, {
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
      "analytics": {
        "appViews": {
          "allTime": 1,
          "lastFourteenDays": 1,
          "lastSevenDays": 1,
          "lastThirtyDays": 1
        },
        "lastViewedAt": "2026-05-07T12:00:00.000Z",
        "publishedResultsUpdatedAt": "2026-05-07T12:00:00.000Z"
      },
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "categories": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creator": {
        "email": "ava@example.com"
      },
      "description": "string",
      "id": "string",
      "lastEditedAt": "2026-05-07T12:00:00.000Z",
      "lastPublishedAt": "2026-05-07T12:00:00.000Z",
      "owner": {
        "email": "ava@example.com"
      },
      "reviews": {
        "required": true
      },
      "schedules": [
        {}
      ],
      "status": "string",
      "title": "string",
      "trashedAt": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hex/latest/actions/list-projects).

## Create Collection



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hex/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hex/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "creator": {
        "email": "ava@example.com",
        "id": "string"
      },
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "sharing": {
        "groups": [
          {}
        ],
        "users": [
          {}
        ],
        "workspace": {}
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Collection action reference](actions/create-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hex/latest/actions/create-collection).
