# Dynalist Universal API Examples

These examples use the MindCloud API key and Dynalist connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Documents And Folders

Retrieves documents and folders from Dynalist.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/list-documents-and-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/list-documents-and-folders?${params}`, {
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
      "_code": "string",
      "_msg": "string",
      "files": [
        {}
      ],
      "root_file_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Documents And Folders action reference](actions/list-documents-and-folders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dynalist/latest/actions/list-documents-and-folders).

## Batch Edit Document Nodes

Updates multiple document nodes in Dynalist.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/batch-edit-document-nodes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string",
  "changes[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/batch-edit-document-nodes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string",
    "changes[]": [{}]
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
      "_code": "string",
      "_msg": "string",
      "new_node_ids": [
        "string"
      ],
      "results": [
        true
      ]
    }
  ],
  "meta": {}
}
```

See the full [Batch Edit Document Nodes action reference](actions/batch-edit-document-nodes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dynalist/latest/actions/batch-edit-document-nodes).
