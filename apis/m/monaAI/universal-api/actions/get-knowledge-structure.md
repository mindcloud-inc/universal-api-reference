# Mona AI: Get Knowledge Structure

Retrieves the knowledge structure from Mona AI.

```
GET https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-knowledge-structure
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mona AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-knowledge-structure?connectionId=$CONNECTION_ID&permission=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "permission": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-knowledge-structure?${params}`, {
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
| `includeItemCounts` | boolean | no | Whether to include item counts in the knowledge structure. |
| `maxDepth` | number | no | Maximum folder depth to return. |
| `permission` | string | yes | Mona permission string required by the knowledge structure endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "structure": [
          {}
        ]
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Knowledge structure result container. |
| `data.structure` | array<object> | Knowledge structure entries. |
| `message` | string | Knowledge structure retrieval status message. |
| `success` | boolean | Whether Mona retrieved the knowledge structure. |

## Native endpoint

Through the native Mona AI API, this operation is `POST /companyKnowledge/getKnowledgeStructure` (base URL `https://api.mona-ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-knowledge-structure.md) for the provider-specific parameters and requirements.

