# Bitskout Universal API Examples

These examples use the MindCloud API key and Bitskout connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Plugins

Retrieves the available plugins from Bitskout.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/list-plugins?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/list-plugins?${params}`, {
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
      "name": "Ava Chen",
      "unique_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Plugins action reference](actions/list-plugins.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bitskout/latest/actions/list-plugins).

## Detect Document Type

Detects a document type with Bitskout.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/detect-document-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "doctype": "legal"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/detect-document-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "doctype": "legal"
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
      "outputs": {
        "Document Type": "string",
        "RawJSON": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Detect Document Type action reference](actions/detect-document-type.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bitskout/latest/actions/detect-document-type).
