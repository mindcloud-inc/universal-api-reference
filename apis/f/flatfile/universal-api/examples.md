# Flatfile Universal API Examples

These examples use the MindCloud API key and Flatfile connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Environments

Retrieves a list of environments from Flatfile.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/list-environments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/list-environments?${params}`, {
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
      "data": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

See the full [List Environments action reference](actions/list-environments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flatfile/latest/actions/list-environments).

## Acknowledge Job

Acknowledges a specific job in Flatfile.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/acknowledge-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "us_job_mindcloud_flatfile"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/acknowledge-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "us_job_mindcloud_flatfile"
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
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Acknowledge Job action reference](actions/acknowledge-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flatfile/latest/actions/acknowledge-job).
