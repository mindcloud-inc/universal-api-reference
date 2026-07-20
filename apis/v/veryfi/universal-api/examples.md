# Veryfi Universal API Examples

These examples use the MindCloud API key and Veryfi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get release notifications

Retrieves release notifications from Veryfi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v1-release-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v1-release-notifications?${params}`, {
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
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get release notifications action reference](actions/get-api-v1-release-notifications.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/veryfi/latest/actions/get-api-v1-release-notifications).

## Process a âDoc

Creates a new AnyDoc in Veryfi.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-any-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-any-documents', {
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
      "details": [
        {}
      ],
      "error": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Process a âDoc action reference](actions/post-api-v8-partner-any-documents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/veryfi/latest/actions/post-api-v8-partner-any-documents).
