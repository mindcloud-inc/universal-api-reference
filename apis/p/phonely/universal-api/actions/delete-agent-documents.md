# Phonely: Delete Agent Documents

Deletes agent documents from Phonely.

```
DELETE https://connect.mindcloud.co/v1/universal/phonely/latest/actions/delete-agent-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/delete-agent-documents?connectionId=$CONNECTION_ID&uid=W4LT4yDethRPfyCn9YAEVeIqrDf1&agentId=nlBwoRo2blPKAKB29rQZ&documentId=document-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "W4LT4yDethRPfyCn9YAEVeIqrDf1",
  "agentId": "nlBwoRo2blPKAKB29rQZ",
  "documentId": "document-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phonely/latest/actions/delete-agent-documents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uid` | string | yes | Your Phonely user ID. Example: `W4LT4yDethRPfyCn9YAEVeIqrDf1`. |
| `agentId` | string | yes | The ID of the agent that owns the document. Example: `nlBwoRo2blPKAKB29rQZ`. |
| `documentId` | string | yes | The ID of the knowledge-base document to delete. Example: `document-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Phonely API, this operation is `DELETE /api/agent-documents` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-agent-documents.md) for the provider-specific parameters and requirements.

