# Rick and Morty: Get Character



```
GET https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/get-character
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rick and Morty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/get-character?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/get-character?${params}`, {
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
| `id` | number | yes | Character identifier. |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string | created |
| `episode` | array | episode |
| `gender` | string | gender |
| `id` | number | id |
| `image` | string | image |
| `location` | object | location |
| `name` | string | name |
| `origin` | object | origin |
| `species` | string | species |
| `status` | string | status |
| `type` | string | type |
| `url` | string | url |

## Native endpoint

Through the native Rick and Morty API, this operation is `GET /character/:id` (base URL `https://rickandmortyapi.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-character.md) for the provider-specific parameters and requirements.

