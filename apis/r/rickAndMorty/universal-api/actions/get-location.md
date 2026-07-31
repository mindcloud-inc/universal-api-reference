# Rick and Morty: Get Location



```
GET https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/get-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rick and Morty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/get-location?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/get-location?${params}`, {
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
| `id` | number | yes | Location identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "dimension": "string",
      "id": 1,
      "name": "Ava Chen",
      "residents": [
        "string"
      ],
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
| `dimension` | string | dimension |
| `id` | number | id |
| `name` | string | name |
| `residents` | array | residents |
| `type` | string | type |
| `url` | string | url |

## Native endpoint

Through the native Rick and Morty API, this operation is `GET /location/:id` (base URL `https://rickandmortyapi.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location.md) for the provider-specific parameters and requirements.

