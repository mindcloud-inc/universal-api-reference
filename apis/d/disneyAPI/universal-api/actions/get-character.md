# Disney API: Get Character



```
GET https://connect.mindcloud.co/v1/universal/disneyAPI/latest/actions/get-character
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Disney API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/disneyAPI/latest/actions/get-character?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/disneyAPI/latest/actions/get-character?${params}`, {
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
| `id` | number | yes | Numeric Disney character ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "_id": 1,
        "films": [
          "string"
        ],
        "imageUrl": "https://example.com",
        "name": "Ava Chen",
        "shortFilms": [
          "string"
        ],
        "sourceUrl": "https://example.com",
        "tvShows": [
          "string"
        ],
        "url": "https://example.com",
        "videoGames": [
          "string"
        ]
      },
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
| `data` | object |  |
| `data._id` | number |  |
| `data.films` | array<string> |  |
| `data.imageUrl` | string |  |
| `data.name` | string |  |
| `data.shortFilms` | array<string> |  |
| `data.sourceUrl` | string |  |
| `data.tvShows` | array<string> |  |
| `data.url` | string |  |
| `data.videoGames` | array<string> |  |
| `info` | object |  |
| `info.count` | number |  |
| `info.nextPage` | string |  |
| `info.previousPage` | string |  |
| `info.totalPages` | number |  |

## Native endpoint

Through the native Disney API API, this operation is `GET /character/:id` (base URL `https://api.disneyapi.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-character.md) for the provider-specific parameters and requirements.

