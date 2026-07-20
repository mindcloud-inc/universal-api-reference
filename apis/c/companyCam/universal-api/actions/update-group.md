# CompanyCam: Update Group



```
PUT https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `group.name` | string | no | The title of the Group |
| `id` | string | yes | ID of the Group |
| `group` | object | no |  |
| `group.users` | list<string> | no | An array of strings containing the UserIDs to add to this group. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "groupUrl": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "users": [
        {
          "companyId": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "emailAddress": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "phoneNumber": "string",
          "status": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "userRole": "string",
          "userUrl": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `createdAt` | date |  |
| `groupUrl` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `users[].companyId` | string |  |
| `users[].createdAt` | date |  |
| `users[].emailAddress` | string |  |
| `users[].firstName` | string |  |
| `users[].id` | string |  |
| `users[].lastName` | string |  |
| `users[].phoneNumber` | string |  |
| `users[].status` | string |  |
| `users[].updatedAt` | date |  |
| `users[].userRole` | string |  |
| `users[].userUrl` | string |  |

## Native endpoint

Through the native CompanyCam API, this operation is `PUT groups/:id` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

