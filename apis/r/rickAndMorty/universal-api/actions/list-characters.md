# Rick and Morty: List Characters



```
GET https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/list-characters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rick and Morty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/list-characters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/list-characters?${params}`, {
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
| `status` | string | no | Filter by alive, dead, or unknown. |
| `species` | string | no | Filter by species. |
| `type` | string | no | Filter by type. |
| `gender` | string | no | Filter by female, male, genderless, or unknown. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "info": {},
      "results": [
        {
          "created": "string",
          "episode": [
            "string"
          ],
          "gender": "string",
          "id": 1,
          "image": "string",
          "location": {},
          "name": "Ava Chen",
          "origin": {},
          "species": "string",
          "status": "string",
          "type": "string",
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
| `results[].created` | string | created |
| `results[].episode` | array | episode |
| `results[].gender` | string | gender |
| `results[].id` | number | id |
| `results[].image` | string | image |
| `results[].location` | object | location |
| `results[].name` | string | name |
| `results[].origin` | object | origin |
| `results[].species` | string | species |
| `results[].status` | string | status |
| `results[].type` | string | type |
| `results[].url` | string | url |

## Native endpoint

Through the native Rick and Morty API, this operation is `GET /character` (base URL `https://rickandmortyapi.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-characters.md) for the provider-specific parameters and requirements.

