# OMDb: Search Titles

Finds titles in OMDb by search term.

```
GET https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/search-titles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OMDb `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/search-titles?connectionId=$CONNECTION_ID&searchTitle=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchTitle": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/search-titles?${params}`, {
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
| `searchTitle` | string | yes | Title text to search across OMDb. |
| `type` | list | no | Restrict search results to a movie, series, or episode. One of: `episode`, `movie`, `series`. |
| `year` | number | no | Release year to narrow the search. |
| `page` | number | no | Results page number to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Response": "string",
      "Search": [
        {}
      ],
      "totalResults": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Response` | string |  |
| `Search` | array<object> |  |
| `totalResults` | string |  |

## Native endpoint

Through the native OMDb API, this operation is `GET /` (base URL `https://www.omdbapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-titles.md) for the provider-specific parameters and requirements.

