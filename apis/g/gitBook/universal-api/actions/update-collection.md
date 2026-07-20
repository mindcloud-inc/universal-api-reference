# GitBook: Update Collection

Updates an existing collection in GitBook.

```
PUT https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/update-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/update-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/update-collection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes |  |
| `defaultLevel` | string | no | Default level applied to the collection. |
| `description` | string | no | Description of the collection. |
| `title` | string | no | Title of the collection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultLevel": "string",
      "description": "string",
      "id": "string",
      "object": "string",
      "organization": "string",
      "permissions": {
        "admin": true,
        "create": true,
        "view": true,
        "viewInviteLinks": true
      },
      "title": "string",
      "urls": {
        "app": "https://example.com",
        "location": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultLevel` | string |  |
| `description` | string |  |
| `id` | string |  |
| `object` | string |  |
| `organization` | string |  |
| `permissions.admin` | boolean |  |
| `permissions.create` | boolean |  |
| `permissions.view` | boolean |  |
| `permissions.viewInviteLinks` | boolean |  |
| `title` | string |  |
| `urls.app` | string |  |
| `urls.location` | string |  |

## Native endpoint

Through the native GitBook API, this operation is `PATCH /collections/:collectionId` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-collection.md) for the provider-specific parameters and requirements.

