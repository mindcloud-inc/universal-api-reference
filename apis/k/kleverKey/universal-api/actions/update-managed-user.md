# KleverKey: Update Managed User



```
PUT https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/update-managed-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KleverKey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/update-managed-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": 1,
  "userId": 1,
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/update-managed-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": 1,
    "userId": 1,
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes |  |
| `userId` | number | yes |  |
| `firstName` | string | yes |  |
| `lastName` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessGroups": [
        {}
      ],
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "organizationIds": [
        1
      ],
      "roles": [
        {}
      ],
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessGroups` | array<object> |  |
| `displayName` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `organizationIds` | array<number> |  |
| `roles` | array<object> |  |
| `type` | number |  |

## Native endpoint

Through the native KleverKey API, this operation is `PUT /api/v1/organizations/:organizationId/users/managed/:userId` (base URL `https://api.kleverkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-managed-user.md) for the provider-specific parameters and requirements.

