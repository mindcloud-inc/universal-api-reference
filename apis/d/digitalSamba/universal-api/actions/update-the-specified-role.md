# Digital Samba: Update the specified role

Updates an existing role in Digital Samba.

```
PUT https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/update-the-specified-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/update-the-specified-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "role": "string",
  "permissions": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/update-the-specified-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "role": "string",
    "permissions": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `role` | string | yes | Role path parameter. |
| `permissions` | object | yes | Must be an array of permissions. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | no | JSON request body documented for this endpoint. |
| `name` | string | no | Must contain only letters, numbers, dashes and underscores. Must not be greater than 30 characters. Must be unique. |
| `displayName` | string | no | Must be at least 3 characters. Must not be greater than 100 characters. |
| `description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "default": true,
      "description": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "permissions": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `default` | boolean |  |
| `description` | string |  |
| `displayName` | string |  |
| `id` | string |  |
| `name` | string |  |
| `permissions` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Digital Samba API, this operation is `PATCH /roles/:role` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-the-specified-role.md) for the provider-specific parameters and requirements.

