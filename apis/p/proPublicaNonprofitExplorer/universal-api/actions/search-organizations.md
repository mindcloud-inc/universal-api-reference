# ProPublica Nonprofit Explorer: Search Organizations

Finds organizations in ProPublica Nonprofit Explorer.

```
GET https://connect.mindcloud.co/v1/universal/proPublicaNonprofitExplorer/latest/actions/search-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProPublica Nonprofit Explorer `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proPublicaNonprofitExplorer/latest/actions/search-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proPublicaNonprofitExplorer/latest/actions/search-organizations?${params}`, {
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
| `q` | string | no | Keyword search string. Searches organization name, alternate name, and city. Supports quoted phrases, +required terms, and -excluded terms per the official API docs. Example: `propublica`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Zero-indexed page number. The API defaults to 0 and returns 25 results per page. Default: `0`. |
| `stateId` | string | no | Two-letter U.S. Postal Service state or territory abbreviation. Use ZZ for entities based outside the United States. Example: `NY`. |
| `nteeId` | number | no | National Taxonomy of Exempt Entities major group integer from 1 through 10. Example: `2`. |
| `taxSectionCode` | number | no | Subsection code under section 501(c), or 92 for 4947(a)(1). For example, 3 means 501(c)(3). Example: `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "api_version": 1,
      "cur_page": 1,
      "data_source": "string",
      "num_pages": 1,
      "organizations": [
        {}
      ],
      "page_offset": 1,
      "per_page": 1,
      "search_query": "string",
      "selected_code": "string",
      "selected_ntee": "string",
      "selected_state": "string",
      "total_results": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_version` | number | Nonprofit Explorer API version. |
| `cur_page` | number | Zero-indexed current page. |
| `data_source` | string | Source citation returned by the API. |
| `num_pages` | number | Number of pages in the result set. |
| `organizations` | array<object> | Organizations matching the search criteria. |
| `page_offset` | number | Number of results before the current page. |
| `per_page` | number | Results returned per page. |
| `search_query` | string | Search query used by the API. |
| `selected_code` | string | Selected tax subsection code filter, if any. |
| `selected_ntee` | string | Selected NTEE major group filter, if any. |
| `selected_state` | string | Selected state filter, if any. |
| `total_results` | number | Total number of matching organizations. |

## Native endpoint

Through the native ProPublica Nonprofit Explorer API, this operation is `GET /search.json` (base URL `https://projects.propublica.org/nonprofits/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-organizations.md) for the provider-specific parameters and requirements.

