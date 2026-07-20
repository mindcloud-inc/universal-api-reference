# Mona AI: Search Company Knowledge

Finds company knowledge in Mona AI.

```
GET https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/search-company-knowledge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mona AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/search-company-knowledge?connectionId=$CONNECTION_ID&permission=string&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "permission": "string",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/search-company-knowledge?${params}`, {
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
| `categories[]` | array<string> | no | Optional knowledge categories to search. |
| `limit` | number | no | Maximum knowledge results to return. |
| `permission` | string | yes | Mona permission string required by the knowledge search endpoint. |
| `query` | string | yes | Knowledge search query. |
| `tags[]` | array<string> | no | Optional knowledge tags to search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "results": [
          {}
        ],
        "searchTerm": "string",
        "totalCount": 1
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
| `data` | object | Knowledge search result container. |
| `data.results` | array<object> | Matching knowledge results. |
| `data.searchTerm` | string | Search term used by Mona. |
| `data.totalCount` | number | Number of matching knowledge results. |
| `message` | string | Knowledge search status message. |
| `success` | boolean | Whether Mona completed the knowledge search. |

## Native endpoint

Through the native Mona AI API, this operation is `POST /companyKnowledge/searchKnowledge` (base URL `https://api.mona-ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-company-knowledge.md) for the provider-specific parameters and requirements.

