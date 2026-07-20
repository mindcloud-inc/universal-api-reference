# SEA-LION AI Playground: Rerank Documents



```
GET https://connect.mindcloud.co/v1/universal/sEALIONAIPlaygroundAPI/latest/actions/rerank-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SEA-LION AI Playground `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sEALIONAIPlaygroundAPI/latest/actions/rerank-documents?connectionId=$CONNECTION_ID&model=string&query=string&documents%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "model": "string",
  "query": "string",
  "documents[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sEALIONAIPlaygroundAPI/latest/actions/rerank-documents?${params}`, {
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
| `model` | string | yes |  |
| `query` | string | yes |  |
| `documents[]` | array<string> | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SEA-LION AI Playground API returns.

## Native endpoint

Through the native SEA-LION AI Playground API, this operation is `POST /rerank` (base URL `https://api.sea-lion.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rerank-documents.md) for the provider-specific parameters and requirements.

