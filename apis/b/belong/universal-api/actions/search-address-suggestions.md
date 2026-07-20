# Belong: Search Address Suggestions

Finds address suggestions in Belong by search text.

```
GET https://connect.mindcloud.co/v1/universal/belong/latest/actions/search-address-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Belong `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/belong/latest/actions/search-address-suggestions?connectionId=$CONNECTION_ID&q=barcelona" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "barcelona"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/belong/latest/actions/search-address-suggestions?${params}`, {
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
| `q` | string | yes | Example: `barcelona`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "formatted_address": "string",
      "id": "string",
      "location": {},
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `description` | string | Address description. |
| `formatted_address` | string | Formatted address string returned by Belong. |
| `id` | string | Belong address ID. |
| `location` | object | GeoJSON location payload. |
| `title` | string | Address title. |
| `updatedAt` | date | Last update timestamp. |
| `userId` | string | Owner user ID. |

## Native endpoint

Through the native Belong API, this operation is `GET /addresses/autocomplete` (base URL `https://api.belong.net/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-address-suggestions.md) for the provider-specific parameters and requirements.

