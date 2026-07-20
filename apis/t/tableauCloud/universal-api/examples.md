# Tableau Cloud Universal API Examples

These examples use the MindCloud API key and Tableau Cloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Query Projects

Retrieves a list of projects from Tableau Cloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-projects?${params}`, {
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
      "contentPermissions": "string",
      "controllingPermissionsProjectId": "string",
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "parentProjectId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Query Projects action reference](actions/query-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tableauCloud/latest/actions/query-projects).

## Add Workbook to Favorites

Adds a workbook to favorites in Tableau Cloud.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/add-workbook-to-favorites" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/add-workbook-to-favorites', {
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
      "contentUrl": "https://example.com",
      "createdAt": "string",
      "label": "string",
      "name": "Ava Chen",
      "updatedAt": "string",
      "viewUrlName": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Workbook to Favorites action reference](actions/add-workbook-to-favorites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tableauCloud/latest/actions/add-workbook-to-favorites).
