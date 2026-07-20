# ScrapingAnt Universal API Examples

These examples use the MindCloud API key and ScrapingAnt connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Credits Usage

Retrieves subscription status and API credits from ScrapingAnt.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/get-api-credits-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/get-api-credits-usage?${params}`, {
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
      "endDate": "2026-05-07T12:00:00.000Z",
      "planName": "Ava Chen",
      "planTotalCredits": 1,
      "remainedCredits": 1,
      "startDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get API Credits Usage action reference](actions/get-api-credits-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapingAnt/latest/actions/get-api-credits-usage).

## Scrape URL With PATCH



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/scrape-url-with-patch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/api/item/123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/scrape-url-with-patch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/api/item/123"
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
      "html": "string"
    }
  ],
  "meta": {}
}
```

See the full [Scrape URL With PATCH action reference](actions/scrape-url-with-patch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapingAnt/latest/actions/scrape-url-with-patch).
