# Scrape do Universal API Examples

These examples use the MindCloud API key and Scrape do connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get usage statistics

Retrieves usage statistics from Scrape do.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-usage-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-usage-statistics?${params}`, {
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
      "ConcurrentRequest": 1,
      "IsActive": true,
      "MaxMonthlyRequest": 1,
      "RemainingConcurrentRequest": 1,
      "RemainingMonthlyRequest": 1
    }
  ],
  "meta": {}
}
```

See the full [Get usage statistics action reference](actions/get-usage-statistics.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapeDo/latest/actions/get-usage-statistics).

## Create async scraping job

Creates a new async scraping job in Scrape do.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/create-async-scraping-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targets[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/create-async-scraping-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targets[]": ["string"]
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
      "JobID": "string",
      "Message": "string",
      "TaskIDs": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create async scraping job action reference](actions/create-async-scraping-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapeDo/latest/actions/create-async-scraping-job).
