# eSign Genie: Create User

Creates a new user in eSign Genie.

```
POST https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eSign Genie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": "string",
      "user": {
        "active": true,
        "companyId": 1,
        "emailId": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "partyId": 1,
        "userRole": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `result` | string |  |
| `user.active` | boolean |  |
| `user.companyId` | number |  |
| `user.emailId` | string |  |
| `user.firstName` | string |  |
| `user.lastName` | string |  |
| `user.partyId` | number |  |
| `user.userRole` | string |  |

## Native endpoint

Through the native eSign Genie API, this operation is `POST /users/create` (base URL `https://na1.foxitesign.foxit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

