# Connecteam: Update Users

Update individual or multiple users associated with the account using the provided details. You can specify updates either by their phone number or unique userID.

```
PUT https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/update-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/update-users" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "users[].userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/update-users', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "users[].userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `editUsersByPhone` | boolean | no | Default: `false`. |
| `includeSmartGroupIds` | boolean | no | Default: `true`. |
| `users[]` | array<object> | no |  |
| `users[].firstName` | string | no |  |
| `users[].lastName` | string | no |  |
| `users[].phoneNumber` | string | no |  |
| `users[].userType` | string | no |  |
| `users[].email` | string | no |  |
| `users[].customFields[]` | array<object> | no |  |
| `users[].customFields[].customFieldId` | number | no |  |
| `users[].customFields[].value` | string | no |  |
| `users[].isArchived` | boolean | no |  |
| `users[].userId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "users": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `users[].createdAt` | number |  |
| `users[].firstName` | string |  |
| `users[].invitedToBeManager` | boolean |  |
| `users[].isArchived` | boolean |  |
| `users[].kioskCode` | string |  |
| `users[].lastLogin` | number |  |
| `users[].lastName` | string |  |
| `users[].modifiedAt` | number |  |
| `users[].phoneNumber` | string |  |
| `users[].smartGroupsIds[]` | number |  |
| `users[].userId` | number |  |
| `users[].userType` | string |  |

## Native endpoint

Through the native Connecteam API, this operation is `PUT /users/v1/users` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-users.md) for the provider-specific parameters and requirements.

