# LinkTwin: Create Link

Creates a new shortened link in LinkTwin.

```
POST https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/create-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/create-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/create-link', {
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
| `url` | string | yes | Long URL to shorten. |
| `custom` | string | no | Custom alias instead of a random alias. |
| `password` | string | no | Password protection for the link. |
| `domain` | string | no | Branded domain that already exists in the account. |
| `expiry` | string | no | Expiration date and time for the link. |
| `clickLimit` | number | no | Maximum number of clicks before the link expires. |
| `expirationRedirect` | string | no | Redirect URL after expiration. |
| `note` | string | no | Internal note for the link. |
| `displayTitle` | string | no | Dashboard-only title for the link. |
| `geoTarget` | object<object> | no | Geo targeting rules. Accepts multiple values as an array. |
| `deviceTarget` | object<object> | no | Device targeting rules. Accepts multiple values as an array. |
| `languageTarget` | object<object> | no | Language targeting rules. Accepts multiple values as an array. |
| `abTesting` | object<object> | no | A/B testing variants. Accepts multiple values as an array. |
| `parameters` | object<object> | no | URL parameters to append. Accepts multiple values as an array. |
| `metaTitle` | string | no | Meta title. |
| `metaDescription` | string | no | Meta description. |
| `metaImage` | string | no | Social share preview image URL. |
| `pixels` | string | no | Pixel IDs or names to attach. Accepts multiple values as an array. |
| `collections` | string | no | Collection IDs or names to add the link to. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "error": 1,
      "id": "string",
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
| `description` | string |  |
| `error` | number |  |
| `id` | string |  |
| `shorturl` | string |  |
| `title` | string |  |

## Native endpoint

Through the native LinkTwin API, this operation is `POST /url/add` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-link.md) for the provider-specific parameters and requirements.

