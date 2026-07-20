# Document AI Universal API Examples

These examples use the MindCloud API key and Document AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Answer Document Questions



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/answer-document-questions?connectionId=$CONNECTION_ID&InputFile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "InputFile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/answer-document-questions?${params}`, {
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
      "answerResults": [
        {}
      ],
      "confidenceScore": 1,
      "successful": true
    }
  ],
  "meta": {}
}
```

See the full [Answer Document Questions action reference](actions/answer-document-questions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/documentAI/latest/actions/answer-document-questions).

## Start Document Classification Batch Job

Creates a document classification batch job in Document AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/start-document-classification-batch-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "InputFile": "string",
  "Categories": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/start-document-classification-batch-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "InputFile": "string",
    "Categories": "string"
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
      "asyncJobID": "string",
      "successful": true
    }
  ],
  "meta": {}
}
```

See the full [Start Document Classification Batch Job action reference](actions/start-document-classification-batch-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/documentAI/latest/actions/start-document-classification-batch-job).
