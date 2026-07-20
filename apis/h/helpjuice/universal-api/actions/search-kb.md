# Helpjuice: Search KB

Finds articles in Helpjuice by search query.

```
GET https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/search-kb
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Helpjuice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/search-kb?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/search-kb?${params}`, {
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
| `query` | string | no | Search text to look up in the knowledge base. |
| `categoryId` | number | no | Optional category ID to scope the search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "searches": [
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
| `meta` | object | Pagination metadata when returned by search. |
| `searches` | array<object> | The Helpjuice search results. |

## Native endpoint

Through the native Helpjuice API, this operation is `GET /search` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-kb.md) for the provider-specific parameters and requirements.

