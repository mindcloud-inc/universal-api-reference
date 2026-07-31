# STAPI: Search Performers



```
GET https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/search-performers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STAPI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/search-performers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/search-performers?${params}`, {
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
| `name` | string | no | Performer name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": {
        "firstPage": true,
        "lastPage": true,
        "numberOfElements": 1,
        "pageNumber": 1,
        "pageSize": 1,
        "totalElements": 1,
        "totalPages": 1
      },
      "performers": [
        {
          "birthName": "Ava Chen",
          "dateOfBirth": "string",
          "gender": "string",
          "name": "Ava Chen",
          "placeOfBirth": "string",
          "uid": "string"
        }
      ],
      "sort": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | object |  |
| `page.firstPage` | boolean |  |
| `page.lastPage` | boolean |  |
| `page.numberOfElements` | number |  |
| `page.pageNumber` | number |  |
| `page.pageSize` | number |  |
| `page.totalElements` | number |  |
| `page.totalPages` | number |  |
| `performers` | array<object> |  |
| `performers[].birthName` | string |  |
| `performers[].dateOfBirth` | string |  |
| `performers[].gender` | string |  |
| `performers[].name` | string |  |
| `performers[].placeOfBirth` | string |  |
| `performers[].uid` | string |  |
| `sort` | object |  |

## Native endpoint

Through the native STAPI API, this operation is `POST /v2/rest/performer/search` (base URL `https://stapi.co/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-performers.md) for the provider-specific parameters and requirements.

