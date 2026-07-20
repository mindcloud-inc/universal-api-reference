# Graphor: Ask Documents With Structured Output

Retrieves structured answers about your documents from Graphor.

```
GET https://connect.mindcloud.co/v1/universal/graphor/latest/actions/ask-documents-with-structured-output
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Graphor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphor/latest/actions/ask-documents-with-structured-output?connectionId=$CONNECTION_ID&outputSchema=string&question=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "outputSchema": "string",
  "question": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphor/latest/actions/ask-documents-with-structured-output?${params}`, {
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
| `outputSchema` | string | yes | Simplified JSON Schema describing the structured output to return. |
| `question` | string | yes | The natural-language question to answer with structured output. |
| `thinkingLevel` | string | no | Optional thinking level: fast, balanced, or accurate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "conversationId": "string",
      "rawJson": "string",
      "structuredOutput": {}
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
| `rawJson` | string |  |
| `structuredOutput` | object |  |

## Native endpoint

Through the native Graphor API, this operation is `POST /ask-sources` (base URL `https://sources.graphorlm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ask-documents-with-structured-output.md) for the provider-specific parameters and requirements.

