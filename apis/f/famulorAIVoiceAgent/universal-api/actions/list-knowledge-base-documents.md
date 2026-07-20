# Famulor AI - Voice Agent: List Knowledge Base Documents

Retrieves documents from a Famulor knowledge base.

```
GET https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/list-knowledge-base-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Famulor AI - Voice Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/list-knowledge-base-documents?connectionId=$CONNECTION_ID&knowledgebaseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "knowledgebaseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/list-knowledge-base-documents?${params}`, {
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
| `knowledgebaseId` | number | yes | Famulor knowledge base ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Knowledge base document records. |

## Native endpoint

Through the native Famulor AI - Voice Agent API, this operation is `GET /user/knowledgebases/:knowledgebaseId/documents` (base URL `https://app.famulor.de/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-knowledge-base-documents.md) for the provider-specific parameters and requirements.

