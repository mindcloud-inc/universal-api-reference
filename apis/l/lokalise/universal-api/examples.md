# Lokalise Universal API Examples

These examples use the MindCloud API key and Lokalise connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects from Lokalise.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/list-projects?${params}`, {
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
      "baseLanguageIso": "string",
      "createdAt": "string",
      "createdByEmail": "ava@example.com",
      "description": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "projectType": "string",
      "teamId": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lokalise/latest/actions/list-projects).

## Create Comments

Creates comments for a Lokalise key.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/create-comments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "key_id": "string",
  "comments": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/create-comments', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "key_id": "string",
    "comments": "string"
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
      "comments": [
        {}
      ],
      "project_id": "string",
      "project_uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Comments action reference](actions/create-comments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lokalise/latest/actions/create-comments).
