# Mindee Universal API Examples

These examples use the MindCloud API key and Mindee connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Job Status

Retrieves a job status from Mindee.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindee/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindee/latest/actions/get-job-status?${params}`, {
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
      "job": {
        "completed_at": "2026-05-07T12:00:00.000Z",
        "created_at": "2026-05-07T12:00:00.000Z",
        "filename": "Ava Chen",
        "id": "string",
        "model_id": "string",
        "polling_url": "https://example.com",
        "result_url": "https://example.com",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Job Status action reference](actions/get-job-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mindee/latest/actions/get-job-status).

## Start Classification Job From URL

Creates a new classification job in Mindee from a URL.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mindee/latest/actions/start-classification-job-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modelId": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mindee/latest/actions/start-classification-job-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modelId": "string",
    "url": "https://example.com"
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
      "job": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "filename": "Ava Chen",
        "id": "string",
        "model_id": "string",
        "polling_url": "https://example.com",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Start Classification Job From URL action reference](actions/start-classification-job-from-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mindee/latest/actions/start-classification-job-from-url).
