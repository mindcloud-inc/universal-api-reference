# Dynamic Content Snippet Universal API Examples

These examples use the MindCloud API key and Dynamic Content Snippet connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve URL Mappings

Retrieves URL mappings from Dynamic Content Snippet.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynamicContentSnippet/latest/actions/retrieve-url-mappings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynamicContentSnippet/latest/actions/retrieve-url-mappings?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "htmlContent": "string",
      "id": "string",
      "isPublished": true,
      "url": "https://example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve URL Mappings action reference](actions/retrieve-url-mappings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dynamicContentSnippet/latest/actions/retrieve-url-mappings).

## Create or Update URL Mapping

Updates a URL mapping in Dynamic Content Snippet, or creates one if needed.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dynamicContentSnippet/latest/actions/create-or-update-url-mapping" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/page",
  "htmlContent": "<div>Hello World</div>"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynamicContentSnippet/latest/actions/create-or-update-url-mapping', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/page",
    "htmlContent": "<div>Hello World</div>"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create or Update URL Mapping action reference](actions/create-or-update-url-mapping.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dynamicContentSnippet/latest/actions/create-or-update-url-mapping).
