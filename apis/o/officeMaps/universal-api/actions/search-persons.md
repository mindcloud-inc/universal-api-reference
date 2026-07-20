# OfficeMaps: Search Persons

Finds people in OfficeMaps by search filters.

```
GET https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/search-persons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeMaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/search-persons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/search-persons?${params}`, {
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
| `searchTerm` | string | no | Filter persons by a general search term. |
| `sort` | string | no | Sort expression for the search results. |
| `pageSize` | number | no | Maximum number of persons per page. |
| `page` | number | no | Page number for the search results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "page": 1,
      "pageSize": 1,
      "skip": 1,
      "sort": "string",
      "top": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | People returned by the search. |
| `page` | number | Current page when provided. |
| `pageSize` | number | Page size when provided. |
| `skip` | number | Skipped record count when provided. |
| `sort` | string | Applied sort expression. |
| `top` | number | Top record count when provided. |
| `total` | number | Total matching people. |

## Native endpoint

Through the native OfficeMaps API, this operation is `GET /v1/person` (base URL `https://api.officemaps.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-persons.md) for the provider-specific parameters and requirements.

