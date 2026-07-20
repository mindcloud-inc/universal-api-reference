# Recut URL Shortener: Get Link

Retrieves link details from Recut URL Shortener.

```
GET https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/get-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/get-link?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/get-link?${params}`, {
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
| `id` | number | yes | Link ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "date": "string",
      "description": "string",
      "device": {},
      "expiry": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "location": {},
      "longurl": "https://example.com",
      "shorturl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string | Short link alias. |
| `date` | string | Creation timestamp. |
| `description` | string | Link description. |
| `device` | object | Device-targeting map. |
| `expiry` | date | Expiration timestamp. |
| `id` | number | Link ID. |
| `location` | object | Geo-targeting location map. |
| `longurl` | string | Destination URL. |
| `shorturl` | string | Short URL. |
| `title` | string | Resolved page title. |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `GET /url/:id` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link.md) for the provider-specific parameters and requirements.

