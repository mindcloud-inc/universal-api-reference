# Documint Universal API Examples

These examples use the MindCloud API key and Documint connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Templates

Retrieves a list of templates from Documint.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documint/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documint/latest/actions/list-templates?${params}`, {
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
      "folder": "string",
      "id": "string",
      "name": "Ava Chen",
      "thumbnail": {}
    }
  ],
  "meta": {}
}
```

See the full [List Templates action reference](actions/list-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/documint/latest/actions/list-templates).

## Merge Template

Creates a document from a template in Documint.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documint/latest/actions/merge-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "69bac297724eda8b0297192e"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documint/latest/actions/merge-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "69bac297724eda8b0297192e"
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
      "_id": "string",
      "account": "string",
      "aws": {},
      "createdAt": "string",
      "dataHash": "string",
      "expiresAt": "string",
      "fileExtension": "string",
      "isLive": true,
      "isTest": true,
      "metadata": {},
      "name": "Ava Chen",
      "template": "string",
      "templateHash": "string",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Merge Template action reference](actions/merge-template.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/documint/latest/actions/merge-template).
