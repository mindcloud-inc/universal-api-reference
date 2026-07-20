# Digital Samba: Create a new role

Creates a new role in Digital Samba.

```
POST https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/create-a-new-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/create-a-new-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "displayName": "Ava Chen",
  "permissions": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/create-a-new-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "displayName": "Ava Chen",
    "permissions": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Must contain only letters, numbers, dashes and underscores. Must not be greater than 30 characters. Must be unique. |
| `displayName` | string | yes | Must be at least 3 characters. Must not be greater than 100 characters. |
| `permissions` | object | yes | Must be an array of permissions. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | no | JSON request body documented for this endpoint. |
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

Through the native Digital Samba API, this operation is `POST /roles` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-new-role.md) for the provider-specific parameters and requirements.

