# Famulor AI - Voice Agent: Get Knowledge Base Document

Retrieves document details from a Famulor knowledge base.

```
GET https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/get-knowledge-base-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Famulor AI - Voice Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/get-knowledge-base-document?connectionId=$CONNECTION_ID&id=1&knowledgebaseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "knowledgebaseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/get-knowledge-base-document?${params}`, {
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
| `id` | number | yes | Knowledge base document ID. |
| `knowledgebaseId` | number | yes | Famulor knowledge base ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Knowledge base document details. |

## Native endpoint

Through the native Famulor AI - Voice Agent API, this operation is `GET /user/knowledgebases/:knowledgebaseId/documents/:id` (base URL `https://app.famulor.de/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-knowledge-base-document.md) for the provider-specific parameters and requirements.

