# AI21 Labs Universal API Examples

These examples use the MindCloud API key and AI21 Labs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Library Files

Retrieves library files from AI21 Labs.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aI21Labs/latest/actions/list-library-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aI21Labs/latest/actions/list-library-files?${params}`, {
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
      "createdBy": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "dataSource": "string",
      "fileId": "string",
      "fileType": "string",
      "labels": [
        "string"
      ],
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "path": "string",
      "publicUrl": "https://example.com",
      "sizeBytes": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Library Files action reference](actions/list-library-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aI21Labs/latest/actions/list-library-files).

## Analyze Sentiment

Creates a sentiment analysis run in AI21 Labs.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aI21Labs/latest/actions/analyze-sentiment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "Paste the customer feedback, review, message, or text to analyze."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aI21Labs/latest/actions/analyze-sentiment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "Paste the customer feedback, review, message, or text to analyze."
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
      "data_sources": [
        {}
      ],
      "error": {},
      "id": "string",
      "requirements_result": {},
      "result": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Analyze Sentiment action reference](actions/analyze-sentiment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aI21Labs/latest/actions/analyze-sentiment).
