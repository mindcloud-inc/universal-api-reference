# Recut URL Shortener: List Channel Items

Retrieves items from a channel in Recut URL Shortener.

```
GET https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-channel-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-channel-items?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-channel-items?${params}`, {
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
| `id` | number | yes | Channel ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "id": 1,
      "link": "https://example.com",
      "preview": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string | Creation date. |
| `id` | number | Item ID. |
| `link` | string | Public item URL. |
| `preview` | string | Preview URL or summary. |
| `title` | string | Item title. |
| `type` | string | Item type. |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `GET /channel/:id` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-channel-items.md) for the provider-specific parameters and requirements.

