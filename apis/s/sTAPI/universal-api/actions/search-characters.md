# STAPI: Search Characters



```
GET https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/search-characters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STAPI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/search-characters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/search-characters?${params}`, {
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
| `name` | string | no | Character name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "characters": [
        {
          "deceased": true,
          "gender": "string",
          "hologram": true,
          "name": "Ava Chen",
          "uid": "string"
        }
      ],
      "page": {
        "firstPage": true,
        "lastPage": true,
        "numberOfElements": 1,
        "pageNumber": 1,
        "pageSize": 1,
        "totalElements": 1,
        "totalPages": 1
      },
      "sort": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `characters` | array<object> |  |
| `characters[].deceased` | boolean |  |
| `characters[].gender` | string |  |
| `characters[].hologram` | boolean |  |
| `characters[].name` | string |  |
| `characters[].uid` | string |  |
| `page` | object |  |
| `page.firstPage` | boolean |  |
| `page.lastPage` | boolean |  |
| `page.numberOfElements` | number |  |
| `page.pageNumber` | number |  |
| `page.pageSize` | number |  |
| `page.totalElements` | number |  |
| `page.totalPages` | number |  |
| `sort` | object |  |

## Native endpoint

Through the native STAPI API, this operation is `POST /v1/rest/character/search` (base URL `https://stapi.co/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-characters.md) for the provider-specific parameters and requirements.

