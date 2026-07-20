# Connecteam: List Users

Retrieves a list of all users associated with the account. Optionally, filter by user ID to receive specific user information

```
GET https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-users?${params}`, {
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
| `limit` | number | no | Default: `10`. |
| `offset` | number | no | Default: `0`. |
| `sort` | string | no |  |
| `order` | string | no |  |
| `userIds` | array<number> | no | Accepts multiple values as an array. |
| `userStatus` | string | no |  |
| `fullNames` | array<string> | no | Accepts multiple values as an array. |
| `phoneNumbers` | array<string> | no | Accepts multiple values as an array. |
| `emailAddresses` | array<string> | no | Accepts multiple values as an array. |
| `createdAt` | number | no |  |
| `modifiedAt` | number | no |  |
| `lastLogin` | number | no |  |
| `archivedAt` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "customFields": [
        {
          "customFieldId": 1,
          "name": "Ava Chen",
          "type": "string",
          "value": "string"
        }
      ],
      "email": "ava@example.com",
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
| `customFields[].customFieldId` | number |  |
| `customFields[].name` | string |  |
| `customFields[].type` | string |  |
| `customFields[].value` | string |  |
| `email` | string |  |
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

Through the native Connecteam API, this operation is `GET /users/v1/users` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

