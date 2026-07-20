# Frontegg: Update Permission

Updates an existing permission in Frontegg.

```
PUT https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-permission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-permission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "permissionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-permission', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "permissionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `permissionId` | string | yes | Permission ID. |
| `key` | string | no | Updated permission key. |
| `name` | string | no | Updated permission name. |
| `description` | string | no | Updated permission description. |
| `categoryId` | string | no | Updated permission category ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": "string",
      "createdAt": "string",
      "description": "string",
      "fePermission": true,
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | string |  |
| `createdAt` | string |  |
| `description` | string |  |
| `fePermission` | boolean |  |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Frontegg API, this operation is `PATCH /identity/resources/permissions/v1/:permissionId` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-permission.md) for the provider-specific parameters and requirements.

