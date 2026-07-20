# eSign Genie: List All Users

Retrieves users from eSign Genie.

```
GET https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eSign Genie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/list-users?${params}`, {
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
      "allActiveUsers": 1,
      "allInactiveUsers": 1,
      "usersList": [
        {
          "active": true,
          "emailId": "ava@example.com",
          "firstName": "Ava",
          "lastName": "Chen",
          "partyId": 1,
          "userRole": "string"
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
| `allActiveUsers` | number |  |
| `allInactiveUsers` | number |  |
| `usersList[].active` | boolean |  |
| `usersList[].emailId` | string |  |
| `usersList[].firstName` | string |  |
| `usersList[].lastName` | string |  |
| `usersList[].partyId` | number |  |
| `usersList[].userRole` | string |  |

## Native endpoint

Through the native eSign Genie API, this operation is `GET /users/list` (base URL `https://na1.foxitesign.foxit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

