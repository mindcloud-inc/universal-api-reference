# Topia: List World Scenes With Dropped Assets

Retrieves scenes and dropped assets from a Topia world.

```
GET https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-world-scenes-with-dropped-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Topia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-world-scenes-with-dropped-assets?connectionId=$CONNECTION_ID&urlSlug=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlSlug": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-world-scenes-with-dropped-assets?${params}`, {
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
| `urlSlug` | string | yes | The Topia world slug. |

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

Through the native Topia API, this operation is `GET /v1/world/:urlSlug/scenes-with-dropped-assets` (base URL `https://api.topia.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-world-scenes-with-dropped-assets.md) for the provider-specific parameters and requirements.

