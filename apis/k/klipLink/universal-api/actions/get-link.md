# KlipLink: Get Link



```
GET https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/get-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KlipLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/get-link?connectionId=$CONNECTION_ID&shortUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shortUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/get-link?${params}`, {
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
| `shortUrl` | string | yes | The short URL identifier, for example klipl.ink/example. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicks": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "destination_url": "https://example.com",
      "id": "string",
      "short_url": "https://example.com",
      "success": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number | Current click count for the link. |
| `created_at` | date | Creation timestamp for the link. |
| `destination_url` | string | Destination URL stored for the link. |
| `id` | string | KlipLink identifier for the link. |
| `short_url` | string | Short URL returned by KlipLink. |
| `success` | boolean | Whether the request succeeded. |
| `title` | string | Title for the link. |

## Native endpoint

Through the native KlipLink API, this operation is `GET /v1/links/:short_url` (base URL `https://api.klipl.ink`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link.md) for the provider-specific parameters and requirements.

