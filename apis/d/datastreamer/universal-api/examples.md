# Datastreamer Universal API Examples

These examples use the MindCloud API key and Datastreamer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Jobs

Finds jobs in Datastreamer by Lucene query.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/search-jobs?connectionId=$CONNECTION_ID&query=%5Bobject%20Object%5D&query.query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "[object Object]",
  "query.query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/search-jobs?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Search Jobs action reference](actions/search-jobs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/datastreamer/latest/actions/search-jobs).

## Create Bluesky Live Feed Job

Creates a Bluesky live feed job in Datastreamer.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/create-bluesky-live-feed-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/create-bluesky-live-feed-job', {
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
  "data": [],
  "meta": {}
}
```

See the full [Create Bluesky Live Feed Job action reference](actions/create-bluesky-live-feed-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/datastreamer/latest/actions/create-bluesky-live-feed-job).
