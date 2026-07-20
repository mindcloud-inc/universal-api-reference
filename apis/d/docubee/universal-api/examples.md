# Docubee Universal API Examples

These examples use the MindCloud API key and Docubee connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Documents

Retrieves documents from Docubee.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-documents?${params}`, {
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
      "createdOn": "string",
      "documentId": "string",
      "name": "Ava Chen",
      "status": "string",
      "tenantId": "string",
      "updatedOn": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Documents action reference](actions/list-documents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docubee/latest/actions/list-documents).

## Create Workflow

Creates a new workflow in Docubee.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/create-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docubee/latest/actions/create-workflow', {
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
      "description": "string",
      "name": "Ava Chen",
      "state": "string",
      "templateId": "string",
      "tenantId": "string",
      "wfModelId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Workflow action reference](actions/create-workflow.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docubee/latest/actions/create-workflow).
