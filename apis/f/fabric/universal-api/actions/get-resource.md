# Fabric: Get Resource

Retrieves a resource from Fabric.

```
GET https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fabric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-resource?connectionId=$CONNECTION_ID&resourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-resource?${params}`, {
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
| `resourceId` | string | yes | The Fabric resource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chats": [
        {}
      ],
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "isLocked": true,
      "isPasswordProtected": true,
      "kind": "string",
      "modifiedAt": "string",
      "name": "Ava Chen",
      "originUrl": "https://example.com",
      "parent": {
        "id": "string",
        "name": "Ava Chen"
      },
      "root": {
        "id": "string",
        "type": "string"
      },
      "stateProcessing": "string",
      "tags": [
        {}
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chats` | array<object> |  |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isLocked` | boolean |  |
| `isPasswordProtected` | boolean |  |
| `kind` | string |  |
| `modifiedAt` | string |  |
| `name` | string |  |
| `originUrl` | string |  |
| `parent.id` | string |  |
| `parent.name` | string |  |
| `root.id` | string |  |
| `root.type` | string |  |
| `stateProcessing` | string |  |
| `tags` | array<object> |  |
| `url` | string |  |

## Native endpoint

Through the native Fabric API, this operation is `GET /v2/resources/{resourceId}` (base URL `https://api.fabric.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource.md) for the provider-specific parameters and requirements.

