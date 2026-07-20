# Phonely: Add Agent Documents

Adds documents to a Phonely agent.

```
POST https://connect.mindcloud.co/v1/universal/phonely/latest/actions/add-agent-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/add-agent-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "W4LT4yDethRPfyCn9YAEVeIqrDf1",
  "agentId": "nlBwoRo2blPKAKB29rQZ",
  "files": "https://example.com/knowledge.txt"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/phonely/latest/actions/add-agent-documents', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uid": "W4LT4yDethRPfyCn9YAEVeIqrDf1",
    "agentId": "nlBwoRo2blPKAKB29rQZ",
    "files": "https://example.com/knowledge.txt"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uid` | string | yes | Your Phonely user ID. Example: `W4LT4yDethRPfyCn9YAEVeIqrDf1`. |
| `agentId` | string | yes | The ID of the agent whose knowledge base will receive the upload. Example: `nlBwoRo2blPKAKB29rQZ`. |
| `files` | file | yes | Document file to upload. Phonely supports PDF, DOCX, and TXT files up to 10 MB each. Example: `https://example.com/knowledge.txt`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentIds": [
        "string"
      ],
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentIds` | array<string> |  |
| `message` | string |  |

## Native endpoint

Through the native Phonely API, this operation is `POST /api/agent-documents` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-agent-documents.md) for the provider-specific parameters and requirements.

