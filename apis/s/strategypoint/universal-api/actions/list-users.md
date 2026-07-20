# Strategypoint: List Users

Retrieves users from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-users?${params}`, {
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
| `count` | number | no | Maximum number of records to return. |
| `email` | string | no | Filter users by email address. |
| `lastEdited` | string | no | Filter by last-edited timestamp. |
| `lastEditedBy` | number | no | Filter by the user who last edited the record. |
| `order` | string | no | Sort order for the result set. |
| `page` | number | no | Page number to return. |

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

Through the native Strategypoint API, this operation is `GET /users` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

