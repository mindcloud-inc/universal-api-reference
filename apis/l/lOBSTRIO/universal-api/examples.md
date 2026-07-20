# LOBSTR.IO Universal API Examples

These examples use the MindCloud API key and LOBSTR.IO connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Crawlers

Retrieves crawlers from LOBSTR.IO.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/list-crawlers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/list-crawlers?${params}`, {
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
      "account": {},
      "creditsPerEmail": {},
      "creditsPerRow": {},
      "defaultWorkerStats": {},
      "description": "string",
      "emailWorkerStats": {},
      "hasEmailVerification": true,
      "hasIssues": true,
      "icon": "string",
      "id": "string",
      "isAvailable": true,
      "isPremium": true,
      "isPublic": true,
      "maxConcurrency": 1,
      "name": "Ava Chen",
      "object": "string",
      "rank": 1,
      "slug": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Crawlers action reference](actions/list-crawlers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lOBSTRIO/latest/actions/list-crawlers).

## Add Tasks

Creates new tasks in LOBSTR.IO.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/add-tasks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "squid": "string",
  "tasks[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/add-tasks', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "squid": "string",
    "tasks[]": [{}]
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
      "duplicatedCount": 1,
      "tasks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Tasks action reference](actions/add-tasks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lOBSTRIO/latest/actions/add-tasks).
