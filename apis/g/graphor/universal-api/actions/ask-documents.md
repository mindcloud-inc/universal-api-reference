# Graphor: Ask Documents

Retrieves answers about your documents from Graphor.

```
GET https://connect.mindcloud.co/v1/universal/graphor/latest/actions/ask-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Graphor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphor/latest/actions/ask-documents?connectionId=$CONNECTION_ID&question=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "question": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphor/latest/actions/ask-documents?${params}`, {
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
| `fileIds` | string | no | Optional list of file IDs to scope the answer to specific documents. |
| `question` | string | yes | The natural-language question to ask about the ingested documents. |
| `thinkingLevel` | string | no | Optional thinking level: fast, balanced, or accurate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "conversationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string |  |
| `conversationId` | string |  |

## Native endpoint

Through the native Graphor API, this operation is `POST /ask-sources` (base URL `https://sources.graphorlm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ask-documents.md) for the provider-specific parameters and requirements.

