# Olostep Universal API Examples

These examples use the MindCloud API key and Olostep connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Answer

Retrieves details for an answer in Olostep.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-answer?connectionId=$CONNECTION_ID&answerId=answer_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "answerId": "answer_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-answer?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "object": "string",
      "result": {
        "jsonContent": "string",
        "jsonHostedUrl": "https://example.com"
      },
      "task": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Answer action reference](actions/get-answer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/olostep/latest/actions/get-answer).

## Complete File Upload

Completes a file upload in Olostep.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/complete-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "file_123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/olostep/latest/actions/complete-file-upload', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "file_123"
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
      "bytes": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "id": "string",
      "object": "string",
      "purpose": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Complete File Upload action reference](actions/complete-file-upload.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/olostep/latest/actions/complete-file-upload).
