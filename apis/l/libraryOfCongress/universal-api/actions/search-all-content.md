# Library of Congress: Search All Content

Finds content across Library of Congress by keyword.

```
GET https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/search-all-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Library of Congress `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/search-all-content?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/search-all-content?${params}`, {
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
| `query` | string | yes | Keyword search across loc.gov metadata and available full text. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `facetFilters` | string | no | Optional loc.gov facet filters such as location:ohio or original-format:periodical\|subject:wildlife. |
| `attributes` | string | no | Optional response attributes to return, for example results, facets, or pagination. |
| `sortBy` | string | no | Optional sort field such as date, date_desc, title_s, or shelf_id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Library of Congress API returns.

## Native endpoint

Through the native Library of Congress API, this operation is `GET /search/` (base URL `https://www.loc.gov`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-all-content.md) for the provider-specific parameters and requirements.

