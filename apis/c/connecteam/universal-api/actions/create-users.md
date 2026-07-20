# Connecteam: Create Users

Create individual or multiple users associated with the account using the provided details.

```
POST https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/create-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/create-users" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "users[].firstName": "Ava",
  "users[].lastName": "Chen",
  "users[].phoneNumber": "string",
  "users[].userType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/create-users', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "users[].firstName": "Ava",
    "users[].lastName": "Chen",
    "users[].phoneNumber": "string",
    "users[].userType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendActivation` | boolean | no | Default: `false`. |
| `users[]` | array<object> | no |  |
| `users[].firstName` | string | yes |  |
| `users[].lastName` | string | yes |  |
| `users[].phoneNumber` | string | yes |  |
| `users[].userType` | string | yes |  |
| `users[].email` | string | no |  |
| `users[].customFields[]` | array<object> | no |  |
| `users[].customFields[].customFieldId` | number | no |  |
| `users[].customFields[].value` | string | no |  |
| `users[].isArchived` | boolean | no | Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "firstName": "Ava",
      "invitedToBeManager": true,
      "isArchived": true,
      "kioskCode": "string",
      "lastLogin": 1,
      "lastName": "Chen",
      "modifiedAt": 1,
      "phoneNumber": "string",
      "smartGroupsIds": [
        1
      ],
      "userId": 1,
      "userType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `firstName` | string |  |
| `invitedToBeManager` | boolean |  |
| `isArchived` | boolean |  |
| `kioskCode` | string |  |
| `lastLogin` | number |  |
| `lastName` | string |  |
| `modifiedAt` | number |  |
| `phoneNumber` | string |  |
| `smartGroupsIds[]` | number |  |
| `userId` | number |  |
| `userType` | string |  |

## Native endpoint

Through the native Connecteam API, this operation is `POST /users/v1/users` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-users.md) for the provider-specific parameters and requirements.

