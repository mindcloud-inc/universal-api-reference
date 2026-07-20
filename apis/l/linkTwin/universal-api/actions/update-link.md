# LinkTwin: Update Link

Updates an existing link in LinkTwin.

```
PUT https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/update-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/update-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/update-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Link ID. |
| `url` | string | no | Long URL to update to. |
| `custom` | string | no | Custom alias. |
| `password` | string | no | Password protection. Send null to remove. |
| `domain` | string | no | Branded domain that already exists in the account. |
| `expiry` | string | no | Expiration date and time. Send null to remove. |
| `clickLimit` | number | no | Maximum number of clicks before the link expires. Send null to remove. |
| `expirationRedirect` | string | no | Redirect URL after expiration. Send null to remove. |
| `note` | string | no | Internal note. Send null to remove. |
| `displayTitle` | string | no | Dashboard-only title. Send null to remove. |
| `geoTarget` | object<object> | no | Geo targeting rules. Send [] to clear all. Accepts multiple values as an array. |
| `deviceTarget` | object<object> | no | Device targeting rules. Send [] to clear all. Accepts multiple values as an array. |
| `languageTarget` | object<object> | no | Language targeting rules. Send [] to clear all. Accepts multiple values as an array. |
| `abTesting` | object<object> | no | A/B testing variants. Send [] to clear all. Accepts multiple values as an array. |
| `parameters` | object<object> | no | URL parameters. Send [] to clear all. Accepts multiple values as an array. |
| `metaTitle` | string | no | Meta title. Send null to remove. |
| `metaDescription` | string | no | Meta description. Send null to remove. |
| `metaImage` | string | no | Social share preview image URL. Send null to remove. |
| `pixels` | string | no | Pixel IDs or names. Send [] to remove all. Accepts multiple values as an array. |
| `collections` | string | no | Collection IDs or names. Send [] to remove from all collections. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "error": 1,
      "id": 1,
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
| `id` | number |  |
| `shorturl` | string |  |
| `title` | string |  |

## Native endpoint

Through the native LinkTwin API, this operation is `PUT /url/:id/update` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-link.md) for the provider-specific parameters and requirements.

