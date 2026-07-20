# Rossum: Retrieve User

Retrieves a user from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-user?${params}`, {
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
| `userID` | string | no | Rossum user ID. |

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

Through the native Rossum API, this operation is `GET /users/:userID` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-user.md) for the provider-specific parameters and requirements.

