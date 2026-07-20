# Webcrawler API Universal API Examples

These examples use the MindCloud API key and Webcrawler API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Feeds

Retrieves all feeds for your organization from Webcrawler API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/list-feeds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/list-feeds?${params}`, {
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
      "createdAt": "string",
      "id": "string",
      "intervalMinutes": 1,
      "itemsLimit": 1,
      "lastRunAt": "string",
      "name": "Ava Chen",
      "nextRunAt": "string",
      "recentRuns": [
        {}
      ],
      "scrapeType": "string",
      "status": "string",
      "url": "https://example.com",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Feeds action reference](actions/list-feeds.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webcrawlerAPI/latest/actions/list-feeds).

## Cancel Crawl Job

Cancels an existing crawl job in Webcrawler API.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/cancel-crawl-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/cancel-crawl-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Crawl Job action reference](actions/cancel-crawl-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webcrawlerAPI/latest/actions/cancel-crawl-job).
