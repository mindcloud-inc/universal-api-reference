# SWAPI: Get Species



```
GET https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-species
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-species?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-species?${params}`, {
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
| `id` | number | yes | The numeric species identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "average_height": "string",
      "classification": "string",
      "designation": "string",
      "language": "string",
      "name": "Ava Chen",
      "skin_colors": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `average_height` | string |  |
| `classification` | string |  |
| `designation` | string |  |
| `language` | string |  |
| `name` | string |  |
| `skin_colors` | string |  |
| `url` | string |  |

## Native endpoint

Through the native SWAPI API, this operation is `GET /species/:id/` (base URL `https://swapi.dev/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-species.md) for the provider-specific parameters and requirements.

