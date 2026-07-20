# Recut URL Shortener: Update Link

Updates an existing link in Recut URL Shortener.

```
PUT https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "url": "https://example.com/updated"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "url": "https://example.com/updated"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | no | Custom domain for the short link. |
| `id` | number | yes | Link ID. |
| `password` | string | no | Password protection for the short link. |
| `type` | string | no | Redirection type or custom splash / CTA overlay identifier. |
| `url` | string | yes | Long URL to shorten. Example: `https://example.com/updated`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `custom` | string | no | Custom alias instead of a random alias. Example: `updated-alias`. |
| `description` | string | no | Note or description for the link. |
| `expiry` | date | no | Expiration timestamp in `YYYY-MM-DD HH:mm:ss` format. |
| `pixels[]` | array<number> | no | Array of pixel IDs. |
| `channel` | number | no | Channel ID to attach to the link. |
| `campaign` | number | no | Campaign ID to attach to the link. |
| `deeplink` | object | no | Object containing app store links and optional `auto` generation flag. |
| `geotarget[]` | array<object> | no | Geo targeting rules as an array of objects with `location` and `link`. |
| `devicetarget[]` | array<object> | no | Device targeting rules as an array of objects with `device` and `link`. |
| `languagetarget[]` | array<object> | no | Language targeting rules as an array of objects with `language` and `link`. |
| `metatitle` | string | no | Open Graph / social title. |
| `metadescription` | string | no | Open Graph / social description. |
| `metaimage` | string | no | Image URL for link previews. |
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
| `id` | number | Updated link ID. |
| `shorturl` | string | Updated shortened URL. |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `PUT /url/:id/update` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-link.md) for the provider-specific parameters and requirements.

