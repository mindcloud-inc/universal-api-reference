# AssemblyAI Universal API Examples

These examples use the MindCloud API key and AssemblyAI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Transcripts

Retrieves transcript records from your AssemblyAI account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/list-transcripts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/list-transcripts?${params}`, {
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
      "pageDetails": {
        "currentUrl": "https://example.com",
        "limit": 1,
        "nextUrl": "https://example.com",
        "prevUrl": "https://example.com",
        "resultCount": 1
      },
      "transcripts": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Transcripts action reference](actions/list-transcripts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/assemblyAI/latest/actions/list-transcripts).

## Process Speech Understanding

Creates speech understanding output from an AssemblyAI transcript.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/process-speech-understanding" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transcriptId": "string",
  "speechUnderstanding": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/process-speech-understanding', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transcriptId": "string",
    "speechUnderstanding": {}
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
      "requestId": "string",
      "speechUnderstanding": {
        "request": {
          "translation": {
            "targetLanguages": [
              [
                "string"
              ]
            ]
          }
        },
        "response": {
          "translation": {
            "status": "string"
          }
        }
      },
      "translatedTexts": {
        "es": "string"
      },
      "utterances": {}
    }
  ],
  "meta": {}
}
```

See the full [Process Speech Understanding action reference](actions/process-speech-understanding.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/assemblyAI/latest/actions/process-speech-understanding).
