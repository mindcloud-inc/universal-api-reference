# Galileo: List Current User Groups

Retrieves groups for the current Galileo user.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-current-user-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-current-user-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-current-user-groups?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "permissions": [
        {
          "action": "string",
          "allowed": true,
          "message": "string"
        }
      ],
      "role": "string",
      "size": 1,
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `permissions` | array<object> |  |
| `permissions[].action` | string |  |
| `permissions[].allowed` | boolean |  |
| `permissions[].message` | string |  |
| `role` | string |  |
| `size` | number |  |
| `visibility` | string |  |

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/current_user/groups` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-current-user-groups.md) for the provider-specific parameters and requirements.

