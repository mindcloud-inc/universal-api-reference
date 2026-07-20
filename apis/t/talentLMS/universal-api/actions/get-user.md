# TalentLMS: Get User

Retrieves a user from a TalentLMS domain.

```
GET https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/get-user?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/get-user?${params}`, {
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
| `id` | number | yes | Numeric user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableTypes": [
        {}
      ],
      "avatar": {},
      "credits": 1,
      "customFields": [
        {}
      ],
      "deactivationDate": "string",
      "description": "string",
      "email": "ava@example.com",
      "emailNotifications": true,
      "id": 1,
      "locale": "string",
      "login": "string",
      "name": "Ava Chen",
      "status": "string",
      "surname": "Ava Chen",
      "timezone": "string",
      "userType": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableTypes` | array<object> |  |
| `avatar` | object |  |
| `credits` | number |  |
| `customFields` | array<object> |  |
| `deactivationDate` | string |  |
| `description` | string |  |
| `email` | string |  |
| `emailNotifications` | boolean |  |
| `id` | number |  |
| `locale` | string |  |
| `login` | string |  |
| `name` | string |  |
| `status` | string |  |
| `surname` | string |  |
| `timezone` | string |  |
| `userType` | object |  |

## Native endpoint

Through the native TalentLMS API, this operation is `GET /users/:id` (base URL `https://{{credentials.domain}}.talentlms.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

