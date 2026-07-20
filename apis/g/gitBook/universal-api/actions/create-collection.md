# GitBook: Create Collection

Creates a new collection in GitBook.

```
POST https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes |  |
| `parent` | string | no |  |
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

Through the native GitBook API, this operation is `POST /orgs/:organizationId/collections` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.

