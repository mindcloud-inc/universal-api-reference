# Agentset Universal API Examples

These examples use the MindCloud API key and Agentset connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Namespaces

Retrieves all namespaces from Agentset.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentset/latest/actions/list-namespaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentset/latest/actions/list-namespaces?${params}`, {
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
        "createdAt": "string",
        "embeddingConfig": {},
        "id": "string",
        "name": "Ava Chen",
        "organizationId": "string",
        "slug": "string",
        "vectorStoreConfig": {}
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Namespaces action reference](actions/list-namespaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agentset/latest/actions/list-namespaces).

## Create Batch Upload URLs

Creates presigned batch file upload URLs in Agentset.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentset/latest/actions/create-batch-upload-urls" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files[]": [
    {}
  ],
  "namespaceId": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentset/latest/actions/create-batch-upload-urls', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files[]": [{}],
    "namespaceId": "Ava Chen"
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
        "key": "string",
        "url": "https://example.com"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Batch Upload URLs action reference](actions/create-batch-upload-urls.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agentset/latest/actions/create-batch-upload-urls).
