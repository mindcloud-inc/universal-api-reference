# JmpTo: Update Link

Updates an existing link in JmpTo.

```
PUT https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaign` | string | no | Campaign ID. |
| `channel` | string | no | Channel ID. |
| `custom` | string | no | Custom alias instead of a random alias. |
| `domain` | string | no | Custom domain for the link. |
| `expiry` | string | no | Expiration timestamp for the link. |
| `id` | number | yes | Link ID to update. |
| `metadescription` | string | no | Meta description for the link. |
| `metaimage` | string | no | URL to a JPG or PNG image. |
| `metatitle` | string | no | Meta title for the link. |
| `password` | string | no | Password protection for the link. |
| `type` | string | no | Redirection type such as direct, frame, or splash. |
| `url` | string | yes | Long URL for the link. |
| `geotarget` | object | no | Geo targeting data. |
| `devicetarget` | object | no | Device targeting data. |
| `languagetarget` | object | no | Language targeting data. |
| `pixels[]` | array<number> | no | Array of pixel IDs. |
| `deeplink` | object | no | Object containing app store links. |

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

Through the native JmpTo API, this operation is `PUT /url/:id/update` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-link.md) for the provider-specific parameters and requirements.

