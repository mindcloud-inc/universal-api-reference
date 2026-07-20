# Scrapi Universal API Examples

These examples use the MindCloud API key and Scrapi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Balance

Retrieves the current API credit balance from Scrapi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapi/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapi/latest/actions/get-balance?${params}`, {
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
      "balance": 1,
      "credits": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Balance action reference](actions/get-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapi/latest/actions/get-balance).

## Scrape Website

Creates a website scrape job in Scrapi.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapi/latest/actions/scrape-website" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapi/latest/actions/scrape-website', {
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
      "reference": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Scrape Website action reference](actions/scrape-website.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapi/latest/actions/scrape-website).
