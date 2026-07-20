# Shorten.REST Universal API Examples

These examples use the MindCloud API key and Shorten.REST connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Aliases by Domain

Retrieves aliases from Shorten.REST for a specific domain.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/list-aliases-by-domain?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/list-aliases-by-domain?${params}`, {
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
      "aliasName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Aliases by Domain action reference](actions/list-aliases-by-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shortenREST/latest/actions/list-aliases-by-domain).

## Create Alias

Creates a new alias in Shorten.REST.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/create-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/create-alias', {
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
      "aliasName": "Ava Chen",
      "domainName": "Ava Chen",
      "shortUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Alias action reference](actions/create-alias.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shortenREST/latest/actions/create-alias).
