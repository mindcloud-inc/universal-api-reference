# Zoho Sprints Universal API Examples

These examples use the MindCloud API key and Zoho Sprints connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves workspaces from Zoho Sprints.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-workspaces?${params}`, {
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
      "baseURL": "https://example.com",
      "createTeamAllowed": true,
      "defaultPortalId": "string",
      "myTeamId": "string",
      "ownerTeamIds": [
        "string"
      ],
      "portals": [
        {}
      ],
      "status": "string",
      "userDisplayName": {}
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoSprints/latest/actions/list-workspaces).

## Add Item Attachments

Adds attachments to an item in Zoho Sprints.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/add-item-attachments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "projectId": "string",
  "sprintId": "string",
  "itemId": "string",
  "uploadfile": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/add-item-attachments', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "projectId": "string",
    "sprintId": "string",
    "itemId": "string",
    "uploadfile": "string"
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Item Attachments action reference](actions/add-item-attachments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoSprints/latest/actions/add-item-attachments).
