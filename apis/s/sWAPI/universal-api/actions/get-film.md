# SWAPI: Get Film



```
GET https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-film
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-film?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-film?${params}`, {
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
| `id` | number | yes | The numeric film identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "characters": [
        "string"
      ],
      "director": "string",
      "episode_id": 1,
      "opening_crawl": "string",
      "producer": "string",
      "release_date": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `characters` | array<string> |  |
| `director` | string |  |
| `episode_id` | number |  |
| `opening_crawl` | string |  |
| `producer` | string |  |
| `release_date` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native SWAPI API, this operation is `GET /films/:id/` (base URL `https://swapi.dev/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-film.md) for the provider-specific parameters and requirements.

