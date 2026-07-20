# ArcSite Universal API Examples

These examples use the MindCloud API key and ArcSite connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Proposal Templates

Retrieves proposal templates from your ArcSite organization.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/list-proposal-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/list-proposal-templates?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Proposal Templates action reference](actions/list-proposal-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/arcSite/latest/actions/list-proposal-templates).

## Add Project Collaborators

Adds collaborators to an existing ArcSite project.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/add-project-collaborators" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "collaborators[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/add-project-collaborators', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "collaborators[]": [{}]
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
      "failItems": [
        {
          "data": {
            "email": "ava@example.com",
            "role": "string"
          },
          "message": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Project Collaborators action reference](actions/add-project-collaborators.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/arcSite/latest/actions/add-project-collaborators).
