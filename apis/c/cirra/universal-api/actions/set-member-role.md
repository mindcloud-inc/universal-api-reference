# Cirra: Set Member Role

Updates a Cirra member role by user ID.

```
PUT https://connect.mindcloud.co/v1/universal/cirra/latest/actions/set-member-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/set-member-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "roleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cirra/latest/actions/set-member-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "roleId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | list | yes |  |
| `roleId` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "isAdmin": true,
      "roleId": "string",
      "user": {
        "email": "ava@example.com",
        "isPending": true,
        "name": "Ava Chen"
      },
      "userId": "string",
      "workflowCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `isAdmin` | boolean |  |
| `roleId` | string |  |
| `user.email` | string |  |
| `user.isPending` | boolean |  |
| `user.name` | string |  |
| `userId` | string |  |
| `workflowCount` | number |  |

## Native endpoint

Through the native Cirra API, this operation is `PUT /v1/members/:userId` (base URL `http://api-public:9801`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-member-role.md) for the provider-specific parameters and requirements.

