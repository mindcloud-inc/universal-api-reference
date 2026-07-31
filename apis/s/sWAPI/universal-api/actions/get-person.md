# SWAPI: Get Person



```
GET https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-person?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-person?${params}`, {
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
| `id` | number | yes | The numeric person identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birth_year": "string",
      "eye_color": "string",
      "films": [
        "string"
      ],
      "gender": "string",
      "hair_color": "string",
      "height": "string",
      "homeworld": "string",
      "mass": "string",
      "name": "Ava Chen",
      "skin_color": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birth_year` | string |  |
| `eye_color` | string |  |
| `films` | array<string> |  |
| `gender` | string |  |
| `hair_color` | string |  |
| `height` | string |  |
| `homeworld` | string |  |
| `mass` | string |  |
| `name` | string |  |
| `skin_color` | string |  |
| `url` | string |  |

## Native endpoint

Through the native SWAPI API, this operation is `GET /people/:id/` (base URL `https://swapi.dev/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

