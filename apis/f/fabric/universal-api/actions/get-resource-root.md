# Fabric: Get Resource Root

Retrieves a resource root from Fabric.

```
GET https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-resource-root
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fabric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-resource-root?connectionId=$CONNECTION_ID&resourceRootId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceRootId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-resource-root?${params}`, {
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
| `resourceRootId` | string | yes | The Fabric resource root ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "folder": {
        "childrenCount": 1,
        "id": "string",
        "isReadonly": true,
        "memberCount": 1,
        "name": "Ava Chen",
        "permissions": {
          "role": "string"
        }
      },
      "id": "string",
      "isPrivate": true,
      "lastResourceAddedAt": "string",
      "modifiedAt": "string",
      "subtype": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `folder.childrenCount` | number |  |
| `folder.id` | string |  |
| `folder.isReadonly` | boolean |  |
| `folder.memberCount` | number |  |
| `folder.name` | string |  |
| `folder.permissions.role` | string |  |
| `id` | string |  |
| `isPrivate` | boolean |  |
| `lastResourceAddedAt` | string |  |
| `modifiedAt` | string |  |
| `subtype` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Fabric API, this operation is `GET /v2/resource-roots/{resourceRootId}` (base URL `https://api.fabric.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource-root.md) for the provider-specific parameters and requirements.

