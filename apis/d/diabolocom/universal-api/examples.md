# Diabolocom Universal API Examples

These examples use the MindCloud API key and Diabolocom connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Job Status

Retrieves a task job status from Diabolocom.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diabolocom/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=job_123&expires=string&signature=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "job_123",
  "expires": "string",
  "signature": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diabolocom/latest/actions/get-job-status?${params}`, {
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
      "data": {
        "correlation_id": "string",
        "id": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Job Status action reference](actions/get-job-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/diabolocom/latest/actions/get-job-status).

## Answer Question

Creates a question answering job in Diabolocom.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/diabolocom/latest/actions/answer-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/diabolocom/latest/actions/answer-question', {
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
  "data": [
    {
      "correlation_id": "string",
      "job_id": "string",
      "job_status_endpoint_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Answer Question action reference](actions/answer-question.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/diabolocom/latest/actions/answer-question).
