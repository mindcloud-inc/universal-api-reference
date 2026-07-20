# Grok: Search Content in Collection

Finds content in a Grok collection by search query.

```
GET https://connect.mindcloud.co/v1/universal/grok/latest/actions/search-content-in-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/search-content-in-collection?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/search-content-in-collection?${params}`, {
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
| `query` | string | yes | Search query text. |
| `source.collectionIds[]` | array<string> | no | Collection IDs to search within. |
| `filter` | string | no | Optional filter expression. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "matches": [
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
| `matches` | array<object> | Document matches returned for the search query. |

## Native endpoint

Through the native Grok API, this operation is `POST /v1/documents/search` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-content-in-collection.md) for the provider-specific parameters and requirements.

