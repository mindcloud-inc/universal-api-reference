# Linkila Universal API Examples

These examples use the MindCloud API key and Linkila connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Filters

Retrieves saved filters from Linkila.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkila/latest/actions/list-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkila/latest/actions/list-filters?${params}`, {
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
      "data": [
        {}
      ],
      "pageInfo": {}
    }
  ],
  "meta": {}
}
```

See the full [List Filters action reference](actions/list-filters.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkila/latest/actions/list-filters).

## Create Redirection Session

Creates a redirection session in Linkila.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkila/latest/actions/create-redirection-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shortURLId": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkila/latest/actions/create-redirection-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shortURLId": "https://example.com"
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
        "session_url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Redirection Session action reference](actions/create-redirection-session.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkila/latest/actions/create-redirection-session).
