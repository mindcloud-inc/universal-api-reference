# Feishu Document Universal API Examples

These examples use the MindCloud API key and Feishu Document connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Block

Retrieves a specific block from a Feishu document.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-block?connectionId=$CONNECTION_ID&blockId=string&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blockId": "string",
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-block?${params}`, {
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
      "code": 1,
      "data": {
        "block": {
          "block_id": "string",
          "block_type": 1,
          "parent_id": "string"
        }
      },
      "msg": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Block action reference](actions/get-block.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/feishuDocument/latest/actions/get-block).

## Create Document

Creates a new document in Feishu Docs.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/create-document', {
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
      "code": 1,
      "data": {
        "document": {
          "document_id": "string",
          "revision_id": 1,
          "title": "string"
        }
      },
      "msg": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Document action reference](actions/create-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/feishuDocument/latest/actions/create-document).
