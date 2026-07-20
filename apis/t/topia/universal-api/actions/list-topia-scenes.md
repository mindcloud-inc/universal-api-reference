# Topia: List Topia Scenes

Retrieves Topia-provided scenes from the shared library.

```
GET https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-topia-scenes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Topia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-topia-scenes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-topia-scenes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "height": 1,
      "id": "string",
      "name": "Ava Chen",
      "topiaKit": true,
      "urlSlug": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created` | date |  |
| `description` | string |  |
| `height` | number |  |
| `id` | string |  |
| `name` | string |  |
| `topiaKit` | boolean |  |
| `urlSlug` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Topia API, this operation is `GET /v1/scenes/topia-scenes` (base URL `https://api.topia.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-topia-scenes.md) for the provider-specific parameters and requirements.

