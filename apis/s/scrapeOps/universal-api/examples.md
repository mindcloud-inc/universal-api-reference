# ScrapeOps Universal API Examples

These examples use the MindCloud API key and ScrapeOps connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Browser Headers

Retrieves fake browser headers from ScrapeOps.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-browser-headers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-browser-headers?${params}`, {
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
      "accept": "string",
      "acceptEncoding": "string",
      "acceptLanguage": "string",
      "secChUa": "string",
      "secChUaMobile": "string",
      "secChUaPlatform": "string",
      "secFetchDest": "string",
      "secFetchMode": "string",
      "secFetchSite": "string",
      "secFetchUser": "string",
      "upgradeInsecureRequests": "string",
      "userAgent": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Browser Headers action reference](actions/list-browser-headers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapeOps/latest/actions/list-browser-headers).

## Create Scheduled Job

Creates a scheduled job in ScrapeOps.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/create-scheduled-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "serverId": 1,
  "serverSpiderId": 1,
  "cronToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/create-scheduled-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "serverId": 1,
    "serverSpiderId": 1,
    "cronToken": "string"
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

See the full [Create Scheduled Job action reference](actions/create-scheduled-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapeOps/latest/actions/create-scheduled-job).
