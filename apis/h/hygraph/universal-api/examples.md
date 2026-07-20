# Hygraph Universal API Examples

These examples use the MindCloud API key and Hygraph connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Introspect Schema

Retrieves GraphQL schema details from Hygraph.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/introspect-schema?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/introspect-schema?${params}`, {
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
      "data": {
        "__schema": {
          "mutationType": {},
          "queryType": {},
          "types": [
            {}
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Introspect Schema action reference](actions/introspect-schema.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hygraph/latest/actions/introspect-schema).

## Create Asset From Remote URL

Creates a new asset from a remote URL in Hygraph.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/create-asset-from-remote-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/create-asset-from-remote-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables": "[object Object]"
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
        "createAsset": {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "fileName": "Ava Chen",
          "handle": "string",
          "id": "string",
          "mimeType": "string",
          "size": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com"
        }
      },
      "extensions": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Asset From Remote URL action reference](actions/create-asset-from-remote-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hygraph/latest/actions/create-asset-from-remote-url).
