# ScrapeGraphAI Universal API Examples

These examples use the MindCloud API key and ScrapeGraphAI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits

Retrieves current credit balance from ScrapeGraphAI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-credits?${params}`, {
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
      "remainingCredits": 1,
      "totalCreditsUsed": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapeGraphAI/latest/actions/get-credits).

## Start Markdownify

Starts a Markdownify conversion job in ScrapeGraphAI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-markdownify" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "websiteUrl": "https://scrapegraphai.com/"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-markdownify', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "websiteUrl": "https://scrapegraphai.com/"
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
      "error": "string",
      "requestId": "string",
      "result": "string",
      "status": "string",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Start Markdownify action reference](actions/start-markdownify.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapeGraphAI/latest/actions/start-markdownify).
