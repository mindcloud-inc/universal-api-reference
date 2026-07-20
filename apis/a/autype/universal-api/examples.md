# Autype Universal API Examples

These examples use the MindCloud API key and Autype connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Key Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autype/latest/actions/get-api-key-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autype/latest/actions/get-api-key-info?${params}`, {
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
      "createdByUserId": "string",
      "creditsAvailable": 1,
      "orgId": "string",
      "orgName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get API Key Info action reference](actions/get-api-key-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/autype/latest/actions/get-api-key-info).

## Create Bulk Render Job From File

Creates a bulk render job from a file in Autype.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/autype/latest/actions/create-bulk-render-job-from-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "file": "string",
  "format": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/autype/latest/actions/create-bulk-render-job-from-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "file": "string",
    "format": "string"
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
      "bulkJobId": "string",
      "completedItems": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "failedItems": 1,
      "format": "string",
      "status": "string",
      "totalItems": 1,
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Bulk Render Job From File action reference](actions/create-bulk-render-job-from-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/autype/latest/actions/create-bulk-render-job-from-file).
