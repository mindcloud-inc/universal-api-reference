# Hasura Universal API Examples

These examples use the MindCloud API key and Hasura connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects from Hasura Cloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasura/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasura/latest/actions/list-projects?${params}`, {
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
        "projects": {
          "endpoint": "string",
          "id": "string",
          "name": "Ava Chen",
          "tenant": {
            "id": "string"
          }
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hasura/latest/actions/list-projects).

## Create Project

Creates a new project in Hasura Cloud.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hasura/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cloud": "aws",
  "region": "us-east-2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hasura/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cloud": "aws",
    "region": "us-east-2"
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
        "createTenant": {
          "id": "string",
          "name": "Ava Chen",
          "tenant": {
            "id": "string",
            "project": {
              "endpoint": "string",
              "id": "string",
              "name": "Ava Chen"
            },
            "slug": "string"
          }
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Project action reference](actions/create-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hasura/latest/actions/create-project).
