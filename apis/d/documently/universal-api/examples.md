# Documently Universal API Examples

These examples use the MindCloud API key and Documently connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects from Documently.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documently/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documently/latest/actions/list-projects?${params}`, {
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
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "hydra:member": [
        {}
      ],
      "hydra:search": {},
      "hydra:totalItems": 1
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/documently/latest/actions/list-projects).

## Create Branch

Creates a new branch in Documently.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documently/latest/actions/create-branch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "project": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documently/latest/actions/create-branch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "project": "string",
    "status": "string"
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
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "author": {},
      "id": "string",
      "name": "Ava Chen",
      "project": "string",
      "sortOrder": [
        "string"
      ],
      "status": "string",
      "storageToBeDeleted": [
        "string"
      ],
      "toBeDeleted": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Branch action reference](actions/create-branch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/documently/latest/actions/create-branch).
