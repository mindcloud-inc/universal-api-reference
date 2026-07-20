# ClearBounce Universal API Examples

These examples use the MindCloud API key and ClearBounce connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Batch Verification Job

Retrieves a batch verification job from ClearBounce.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearBounce/latest/actions/get-batch-verification-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearBounce/latest/actions/get-batch-verification-job?${params}`, {
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
      "job": {},
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Get Batch Verification Job action reference](actions/get-batch-verification-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clearBounce/latest/actions/get-batch-verification-job).

## Create Batch Verification Job

Creates a batch verification job in ClearBounce.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clearBounce/latest/actions/create-batch-verification-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clearBounce/latest/actions/create-batch-verification-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": ["ava@example.com"]
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
      "duplicateCount": 1,
      "emptyRows": 1,
      "estimatedTimeSeconds": 1,
      "invalidRows": 1,
      "jobId": "string",
      "skippedRows": 1,
      "success": true,
      "totalEmails": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Batch Verification Job action reference](actions/create-batch-verification-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clearBounce/latest/actions/create-batch-verification-job).
