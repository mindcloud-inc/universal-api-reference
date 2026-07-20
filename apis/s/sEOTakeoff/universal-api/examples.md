# SEOTakeoff Universal API Examples

These examples use the MindCloud API key and SEOTakeoff connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Jobs



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/list-jobs?connectionId=$CONNECTION_ID&tenantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tenantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/list-jobs?${params}`, {
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
      "count": 1,
      "jobs": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List Jobs action reference](actions/list-jobs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sEOTakeoff/latest/actions/list-jobs).

## Create Generation Job



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/create-generation-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tenantId": "string",
  "headline": "string",
  "keyword": "string",
  "cluster": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/create-generation-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tenantId": "string",
    "headline": "string",
    "keyword": "string",
    "cluster": "string"
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "estimated_time_seconds": 1,
      "job_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Generation Job action reference](actions/create-generation-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sEOTakeoff/latest/actions/create-generation-job).
