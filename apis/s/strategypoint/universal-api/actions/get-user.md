# Strategypoint: Get User

Retrieves a user from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-user?${params}`, {
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
| `userId` | number | yes | The unique user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "department": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "lastLoginDate": "string",
      "lastName": "Chen",
      "title": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `department` | string | The user's department. |
| `email` | string | The user's email address. |
| `firstName` | string | The user's first name. |
| `fullName` | string | The user's full name. |
| `lastLoginDate` | string | The user's last login timestamp. |
| `lastName` | string | The user's last name. |
| `title` | string | The user's job title. |
| `userId` | number | The unique user identifier. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /users/{userId}` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

