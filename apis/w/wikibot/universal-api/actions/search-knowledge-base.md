# Wikibot: Search Knowledge Base

Finds knowledge base articles in Wikibot by search query.

```
GET https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/search-knowledge-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wikibot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/search-knowledge-base?connectionId=$CONNECTION_ID&q=How%20do%20I%20reset%20my%20password%3F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "How do I reset my password?"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/search-knowledge-base?${params}`, {
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
| `q` | string | yes | Search query. Example: `How do I reset my password?`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | string | no | Number of records to skip. Example: `0`. |
| `take` | string | no | Number of records to return. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articles": [
        {
          "content": "string",
          "indexedAt": "string",
          "link": "https://example.com",
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articles` | array<object> | Relevant knowledge base article results. |
| `articles[].content` | string | Article content excerpt. |
| `articles[].indexedAt` | string | Indexed timestamp. |
| `articles[].link` | string | Article link. |
| `articles[].title` | string | Article title. |

## Native endpoint

Through the native Wikibot API, this operation is `GET /bot/search` (base URL `https://api.wikibot.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-knowledge-base.md) for the provider-specific parameters and requirements.

