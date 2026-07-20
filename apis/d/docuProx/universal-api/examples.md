# DocuProx Universal API Examples

These examples use the MindCloud API key and DocuProx connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Job Status



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuProx/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuProx/latest/actions/get-job-status?${params}`, {
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

See the full [Get Job Status action reference](actions/get-job-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docuProx/latest/actions/get-job-status).

## Create Processing Job



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuProx/latest/actions/create-processing-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actualImage": "string",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuProx/latest/actions/create-processing-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actualImage": "string",
    "templateId": "string"
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

See the full [Create Processing Job action reference](actions/create-processing-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docuProx/latest/actions/create-processing-job).
