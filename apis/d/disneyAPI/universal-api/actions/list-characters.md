# Disney API: List Characters



```
GET https://connect.mindcloud.co/v1/universal/disneyAPI/latest/actions/list-characters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Disney API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/disneyAPI/latest/actions/list-characters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/disneyAPI/latest/actions/list-characters?${params}`, {
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
| `name` | string | no | Character name filter documented by Disney API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "_id": 1,
          "films": [
            "string"
          ],
          "imageUrl": "https://example.com",
          "name": "Ava Chen",
          "tvShows": [
            "string"
          ],
          "url": "https://example.com"
        }
      ],
      "info": {
        "count": 1,
        "nextPage": "string",
        "previousPage": "string",
        "totalPages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[]._id` | number |  |
| `data[].films` | array<string> |  |
| `data[].imageUrl` | string |  |
| `data[].name` | string |  |
| `data[].tvShows` | array<string> |  |
| `data[].url` | string |  |
| `info` | object |  |
| `info.count` | number |  |
| `info.nextPage` | string |  |
| `info.previousPage` | string |  |
| `info.totalPages` | number |  |

## Native endpoint

Through the native Disney API API, this operation is `GET /character` (base URL `https://api.disneyapi.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-characters.md) for the provider-specific parameters and requirements.

