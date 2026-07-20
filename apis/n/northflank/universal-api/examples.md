# Northflank Universal API Examples

These examples use the MindCloud API key and Northflank connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List projects

Retrieves projects for the authenticated Northflank account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/northflank/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/northflank/latest/actions/list-projects?${params}`, {
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
        "projects": [
          {
            "description": "string",
            "id": "string",
            "name": "Ava Chen"
          }
        ]
      },
      "pagination": {
        "count": 1,
        "cursor": "string",
        "hasNextPage": true
      }
    }
  ],
  "meta": {}
}
```

See the full [List projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/northflank/latest/actions/list-projects).

## Build service

Starts a new build for a Northflank service.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/northflank/latest/actions/build-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/northflank/latest/actions/build-service', {
  method: 'POST',
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
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Build service action reference](actions/build-service.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/northflank/latest/actions/build-service).
