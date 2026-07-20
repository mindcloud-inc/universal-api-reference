# JmpTo: Shorten Link

Creates a shortened link in JmpTo.

```
POST https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/shorten-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/shorten-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/shorten-link', {
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
| `description` | string | no | Note or description for the short link. |
| `metadescription` | string | no | Meta description for the short link. |
| `metaimage` | string | no | URL to a JPG or PNG image. |
| `metatitle` | string | no | Meta title for the short link. |
| `url` | string | yes | Long URL to shorten. |
| `custom` | string | no | Custom alias instead of a random alias. |
| `type` | string | no | Redirection type such as direct, frame, or splash. |
| `password` | string | no | Password protection for the short link. |
| `domain` | string | no | Custom domain for the short link. |
| `expiry` | string | no | Expiration timestamp for the link. |
| `geotarget` | object | no | Geo targeting data. |
| `devicetarget` | object | no | Device targeting data. |
| `languagetarget` | object | no | Language targeting data. |
| `pixels[]` | array<number> | no | Array of pixel IDs. |
| `channel` | number | no | Channel ID. |
| `campaign` | number | no | Campaign ID. |
| `deeplink` | object | no | Object containing app store links. |
| `status` | string | no | Link status, public or private. |

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
| `error` | number | Provider success/error code. |
| `id` | number | Link ID. |
| `shorturl` | string | Shortened URL. |

## Native endpoint

Through the native JmpTo API, this operation is `POST /url/add` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/shorten-link.md) for the provider-specific parameters and requirements.

