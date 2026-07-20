# DocMaker Universal API Examples

These examples use the MindCloud API key and DocMaker connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Job Result File Details

Retrieves result file details from a DocMaker job.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/get-job-result-file-details?connectionId=$CONNECTION_ID&jobId=7f901fa7-4cb5-46d3-9a83-c9f5a0c860a2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "7f901fa7-4cb5-46d3-9a83-c9f5a0c860a2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/get-job-result-file-details?${params}`, {
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
      "createdAt": 1,
      "jobId": "string",
      "jsonRequest": "string",
      "name": "Ava Chen",
      "remaining_credits": 1,
      "result_file": "string",
      "route": "string",
      "status": "string",
      "status_code": 1,
      "updatedAt": 1,
      "userId": "string",
      "workflowID": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Job Result File Details action reference](actions/get-job-result-file-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docMaker/latest/actions/get-job-result-file-details).

## Create DOCX from DOCX Template URL

Creates a DOCX from a DOCX template URL in DocMaker.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/create-docx-from-docx-template-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "templateUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/create-docx-from-docx-template-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "templateUrl": "https://example.com"
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create DOCX from DOCX Template URL action reference](actions/create-docx-from-docx-template-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docMaker/latest/actions/create-docx-from-docx-template-url).
