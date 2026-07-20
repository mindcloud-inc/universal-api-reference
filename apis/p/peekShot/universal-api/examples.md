# PeekShot Universal API Examples

These examples use the MindCloud API key and PeekShot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects from PeekShot with optional filtering.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/list-projects?${params}`, {
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
      "data": {
        "meta": {
          "currentPage": 1,
          "limit": 1,
          "totalProjects": 1
        },
        "projects": [
          {}
        ]
      },
      "message": "string",
      "status": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/peekShot/latest/actions/list-projects).

## Create Screenshot from HTML

Creates a screenshot from HTML in PeekShot.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/create-screenshot-from-html" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/create-screenshot-from-html', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "html": "string"
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
      "data": {
        "creditRequired": 1,
        "organizationId": 1,
        "requestId": 1
      },
      "message": "string",
      "status": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Screenshot from HTML action reference](actions/create-screenshot-from-html.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/peekShot/latest/actions/create-screenshot-from-html).
