# Ainoflow Convert Universal API Examples

These examples use the MindCloud API key and Ainoflow Convert connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Job Status

Retrieves conversion job status and download URLs from Ainoflow Convert.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=00000000-0000-0000-0000-000000000000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "00000000-0000-0000-0000-000000000000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/get-job-status?${params}`, {
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
      "completedAt": "string",
      "createdAt": "string",
      "expiryAt": "string",
      "files": [
        {
          "models": "string",
          "text": {
            "expiration": "string",
            "url": "https://example.com"
          }
        }
      ],
      "id": "string",
      "models": "string",
      "processingTimeInSeconds": 1,
      "reference": "string",
      "responseMode": "string",
      "startedAt": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Job Status action reference](actions/get-job-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ainoflowConvert/latest/actions/get-job-status).

## Submit Base64 Document

Creates a conversion job in Ainoflow Convert from base64 content.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/submit-base64-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentBase64": "JVBERi0xLjQK...",
  "languages": "en,de",
  "outputs": "text,pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/submit-base64-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentBase64": "JVBERi0xLjQK...",
    "languages": "en,de",
    "outputs": "text,pdf"
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
      "files": [
        {
          "models": "string",
          "text": {
            "expiration": "string",
            "url": "https://example.com"
          }
        }
      ],
      "id": "string",
      "models": "string",
      "processingTimeInSeconds": 1,
      "reference": "string",
      "responseMode": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Submit Base64 Document action reference](actions/submit-base64-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ainoflowConvert/latest/actions/submit-base64-document).
