# GitBook: Get Collection

Retrieves a collection's details from GitBook.

```
GET https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/get-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/get-collection?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/get-collection?${params}`, {
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
| `collectionId` | string | yes |  |

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

Through the native GitBook API, this operation is `GET /collections/:collectionId` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection.md) for the provider-specific parameters and requirements.

