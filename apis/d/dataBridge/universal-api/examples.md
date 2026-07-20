# DataBridge Universal API Examples

These examples use the MindCloud API key and DataBridge connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Available Models

Retrieves available models from DataBridge.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/get-available-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/get-available-models?${params}`, {
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
      "chatModels": [
        {}
      ],
      "defaultModels": {},
      "embeddingModels": [
        {}
      ],
      "providers": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Available Models action reference](actions/get-available-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataBridge/latest/actions/get-available-models).

## Add Document To Folder

Adds a document to a folder in DataBridge.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/add-document-to-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/add-document-to-folder', {
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
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Document To Folder action reference](actions/add-document-to-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataBridge/latest/actions/add-document-to-folder).
