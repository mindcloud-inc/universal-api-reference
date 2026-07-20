# Rossum: Update User

Updates a user in Rossum.

```
PUT https://connect.mindcloud.co/v1/universal/rossum/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userID": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rossum/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userID": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userID` | number | yes | Rossum user ID. |
| `lastName` | string | no | Updated user last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authType": "string",
      "dateJoined": "string",
      "deleted": true,
      "email": "ava@example.com",
      "emailVerified": true,
      "firstName": "Ava",
      "id": 1,
      "isActive": true,
      "lastLogin": {},
      "lastName": "Chen",
      "oidcId": {},
      "organization": "string",
      "phoneNumber": {},
      "uiSettings": {
        "complexLineItems": true
      },
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authType` | string |  |
| `dateJoined` | string |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `emailVerified` | boolean |  |
| `firstName` | string |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `lastLogin` | object |  |
| `lastName` | string |  |
| `oidcId` | object |  |
| `organization` | string |  |
| `phoneNumber` | object |  |
| `uiSettings.complexLineItems` | boolean |  |
| `url` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `PATCH /users/:userID` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

