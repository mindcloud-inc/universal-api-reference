# Diffy Universal API Examples

These examples use the MindCloud API key and Diffy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves the project list from Diffy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffy/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffy/latest/actions/list-projects?${params}`, {
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
      "id": 1,
      "name": "Ava Chen",
      "schedule": "string",
      "urlsCount": 1
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/diffy/latest/actions/list-projects).

## Compare Environments

Creates an environment comparison diff in Diffy.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/diffy/latest/actions/compare-environments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "env1": "string",
  "env2": "string",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/diffy/latest/actions/compare-environments', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "env1": "string",
    "env2": "string",
    "id": 1
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
      "response": 1
    }
  ],
  "meta": {}
}
```

See the full [Compare Environments action reference](actions/compare-environments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/diffy/latest/actions/compare-environments).
