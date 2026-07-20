# profileAPI Universal API Examples

These examples use the MindCloud API key and profileAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Company Find Jobs

Retrieves company search jobs from profileAPI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/list-company-find-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/list-company-find-jobs?${params}`, {
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
      "error": {
        "code": 1,
        "message": "string"
      },
      "jobId": "string",
      "progress": 1,
      "requestedAt": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Company Find Jobs action reference](actions/list-company-find-jobs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/profileAPI/latest/actions/list-company-find-jobs).

## Create Company Find Job

Creates a company search job in profileAPI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/create-company-find-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filters": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/create-company-find-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filters": "[object Object]"
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
      "jobId": "string",
      "jobUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Company Find Job action reference](actions/create-company-find-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/profileAPI/latest/actions/create-company-find-job).
