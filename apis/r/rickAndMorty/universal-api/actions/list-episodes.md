# Rick and Morty: List Episodes



```
GET https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/list-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rick and Morty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/list-episodes?${params}`, {
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
| `page` | number | no | Page of results. |
| `name` | string | no | Filter by name. |
| `episode` | string | no | Filter by episode code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "info": {},
      "results": [
        {
          "air_date": "string",
          "characters": [
            "string"
          ],
          "created": "string",
          "episode": "string",
          "id": 1,
          "name": "Ava Chen",
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `info` | object | Pagination metadata. |
| `results` | array<object> | Resource results. |
| `results[].air_date` | string | air_date |
| `results[].characters` | array | characters |
| `results[].created` | string | created |
| `results[].episode` | string | episode |
| `results[].id` | number | id |
| `results[].name` | string | name |
| `results[].url` | string | url |

## Native endpoint

Through the native Rick and Morty API, this operation is `GET /episode` (base URL `https://rickandmortyapi.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episodes.md) for the provider-specific parameters and requirements.

