# Recut URL Shortener: Shorten Link

Creates a shortened link in Recut URL Shortener.

```
POST https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/shorten-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/shorten-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/shorten-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Long URL to shorten. Example: `https://example.com`. |
| `custom` | string | no | Custom alias instead of a random alias. Example: `my-custom-alias`. |
| `status` | string | no | Link visibility: `public` or `private`. Example: `private`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Note or description for the link. |
| `type` | string | no | Redirection type or custom splash / CTA overlay identifier. |
| `password` | string | no | Password protection for the short link. |
| `domain` | string | no | Custom domain for the short link. |
| `expiry` | date | no | Expiration timestamp in `YYYY-MM-DD HH:mm:ss` format. |
| `metatitle` | string | no | Open Graph / social title. |
| `metadescription` | string | no | Open Graph / social description. |
| `metaimage` | string | no | Image URL for link previews. |
| `pixels[]` | array<number> | no | Array of pixel IDs. |
| `channel` | number | no | Channel ID to attach to the link. |
| `campaign` | number | no | Campaign ID to attach to the link. |
| `deeplink` | object | no | Object containing app store links and optional `auto` generation flag. |
| `geotarget[]` | array<object> | no | Geo targeting rules as an array of objects with `location` and `link`. |
| `devicetarget[]` | array<object> | no | Device targeting rules as an array of objects with `device` and `link`. |
| `languagetarget[]` | array<object> | no | Language targeting rules as an array of objects with `language` and `link`. |
| `parameters[]` | array<object> | no | Additional URL parameters as an array of objects from the docs example. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": 1,
      "id": 1,
      "shorturl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | number | Recut API error flag. |
| `id` | number | Created link ID. |
| `shorturl` | string | Created shortened URL. |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `POST /url/add` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/shorten-link.md) for the provider-specific parameters and requirements.

