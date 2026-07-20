# Blaze AI Universal API Examples

These examples use the MindCloud API key and Blaze AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves available workspaces from Blaze AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-workspaces?${params}`, {
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
      "data": [
        {
          "domain": "string",
          "id": 1,
          "logoUrl": "https://example.com",
          "name": "Ava Chen"
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blazeAI/latest/actions/list-workspaces).

## Add Doc Access

Creates a document access in Blaze AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/add-doc-access" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace_id": "994619",
  "doc_id": "4981633",
  "permission": "edit",
  "accessorType": "Group",
  "accessorId": "994233"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/add-doc-access', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace_id": "994619",
    "doc_id": "4981633",
    "permission": "edit",
    "accessorType": "Group",
    "accessorId": "994233"
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
        "accessorId": 1,
        "accessorType": "string",
        "docId": 1,
        "id": 1,
        "inherited": true,
        "permission": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Doc Access action reference](actions/add-doc-access.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blazeAI/latest/actions/add-doc-access).
