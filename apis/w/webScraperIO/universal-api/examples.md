# WebScraper.IO Universal API Examples

These examples use the MindCloud API key and WebScraper.IO connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves your WebScraper.IO account details and credits.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/get-account-info?${params}`, {
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
      "email": "ava@example.com",
      "firstname": "Ava",
      "lastname": "Chen",
      "pageCredits": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webScraperIO/latest/actions/get-account-info).

## Create Scraping Job

Creates a new scraping job in WebScraper.IO.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/create-scraping-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driver": "string",
  "pageLoadDelay": 1,
  "proxy": "string",
  "requestInterval": 1,
  "sitemapId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/create-scraping-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driver": "string",
    "pageLoadDelay": 1,
    "proxy": "string",
    "requestInterval": 1,
    "sitemapId": 1
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
      "customId": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Scraping Job action reference](actions/create-scraping-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webScraperIO/latest/actions/create-scraping-job).
