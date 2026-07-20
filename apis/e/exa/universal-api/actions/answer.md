# Exa: Answer

Retrieves an answer from Exa.

```
GET https://connect.mindcloud.co/v1/universal/exa/latest/actions/answer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/answer?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exa/latest/actions/answer?${params}`, {
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
| `query` | string | yes | The question or query to answer. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stream` | boolean | no | If true, the response is returned as a server-sent events (SSS) stream. Default: `false`. |
| `text` | boolean | no | If true, the response includes full text content in the search results Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "citations": {
        "author": "string",
        "favicon": "string",
        "id": "string",
        "image": "string",
        "publishedDate": "2026-05-07T12:00:00.000Z",
        "text": "string",
        "title": "string",
        "url": "https://example.com"
      },
      "costDollars": {
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string |  |
| `citations` | array<object> |  |
| `citations.author` | string |  |
| `citations.favicon` | string |  |
| `citations.id` | string |  |
| `citations.image` | string |  |
| `citations.publishedDate` | date |  |
| `citations.text` | string |  |
| `citations.title` | string |  |
| `citations.url` | string |  |
| `costDollars` | object |  |
| `costDollars.total` | number |  |

## Native endpoint

Through the native Exa API, this operation is `POST /answer` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/answer.md) for the provider-specific parameters and requirements.

