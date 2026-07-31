# icanhazdadjoke: Search Dad Jokes

Finds dad jokes in icanhazdadjoke by search term.

```
GET https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/search-dad-jokes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a icanhazdadjoke `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/search-dad-jokes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/search-dad-jokes?${params}`, {
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
| `term` | string | no | Optional search term to use when searching dad jokes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_page": 1,
      "limit": 1,
      "next_page": 1,
      "previous_page": 1,
      "results": [
        {}
      ],
      "search_term": "string",
      "status": 1,
      "total_jokes": 1,
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | number | Current result page. |
| `limit` | number | Results per page. |
| `next_page` | number | Next result page. |
| `previous_page` | number | Previous result page. |
| `results` | array<object> | Matching dad jokes, each with id and joke. |
| `search_term` | string | Submitted search term. |
| `status` | number | HTTP-style status from the API response. |
| `total_jokes` | number | Total matching jokes. |
| `total_pages` | number | Total result pages. |

## Native endpoint

Through the native icanhazdadjoke API, this operation is `GET /search` (base URL `https://icanhazdadjoke.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-dad-jokes.md) for the provider-specific parameters and requirements.

