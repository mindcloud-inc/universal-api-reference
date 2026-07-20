# Shuffll Universal API Examples

These examples use the MindCloud API key and Shuffll connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves organizations from Shuffll.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-organizations?${params}`, {
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
      "branding": {},
      "id": "string",
      "isAllowedToUseOrganization": true,
      "isDefaultForUser": true,
      "name": "Ava Chen",
      "userCount": 1,
      "workspaces": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shuffll/latest/actions/list-organizations).

## Create Asset Folder

Creates a new asset folder in Shuffll.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/create-asset-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "newName": "Ava Chen",
  "organizationId": "69cac8104c4a701fd26271a1",
  "workspaceId": "69cac8104c4a701fd26271a5"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/create-asset-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "newName": "Ava Chen",
    "organizationId": "69cac8104c4a701fd26271a1",
    "workspaceId": "69cac8104c4a701fd26271a5"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Asset Folder action reference](actions/create-asset-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shuffll/latest/actions/create-asset-folder).
