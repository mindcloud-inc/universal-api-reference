# Retell AI Universal API Examples

These examples use the MindCloud API key and Retell AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Voices

Retrieves voices from Retell AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-voices?${params}`, {
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
      "accent": "string",
      "age": "string",
      "avatarUrl": "https://example.com",
      "gender": "string",
      "previewAudioUrl": "https://example.com",
      "provider": "string",
      "recommended": true,
      "standardVoiceType": "string",
      "voiceId": "string",
      "voiceName": "Ava Chen",
      "voiceType": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Voices action reference](actions/list-voices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/retellAI/latest/actions/list-voices).

## Add Knowledge Base Sources

Adds sources to a knowledge base in Retell AI.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/add-knowledge-base-sources" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "knowledgeBaseId": "string",
  "knowledgeBaseTexts[].title": "string",
  "knowledgeBaseTexts[].text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/add-knowledge-base-sources', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "knowledgeBaseId": "string",
    "knowledgeBaseTexts[].title": "string",
    "knowledgeBaseTexts[].text": "string"
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
      "enableAutoRefresh": true,
      "knowledgeBaseId": "string",
      "knowledgeBaseName": "Ava Chen",
      "knowledgeBaseSources": [
        {
          "filename": "Ava Chen",
          "fileUrl": "https://example.com",
          "sourceId": "string",
          "type": "string"
        }
      ],
      "lastRefreshedTimestamp": 1,
      "maxChunkSize": 1,
      "minChunkSize": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Knowledge Base Sources action reference](actions/add-knowledge-base-sources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/retellAI/latest/actions/add-knowledge-base-sources).
