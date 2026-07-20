# TalentLMS: List Users

Retrieves users from a TalentLMS domain.

```
GET https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/list-users?${params}`, {
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
| `pageNumber` | number | no | Page number for paginated results (starts at 1). |
| `pageSize` | number | no | Number of records per page (max 100). Default: `10`. |
| `login` | string | no | Filter users by exact login. |
| `email` | string | no | Filter users by exact email. |
| `customFieldValue` | string | no | Filter users by custom field value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": {},
      "email": "ava@example.com",
      "id": 1,
      "lastLogin": "string",
      "lastUpdated": "string",
      "login": "string",
      "name": "Ava Chen",
      "registration": "string",
      "status": "string",
      "surname": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | object |  |
| `email` | string |  |
| `id` | number |  |
| `lastLogin` | string |  |
| `lastUpdated` | string |  |
| `login` | string |  |
| `name` | string |  |
| `registration` | string |  |
| `status` | string |  |
| `surname` | string |  |
| `type` | string |  |

## Native endpoint

Through the native TalentLMS API, this operation is `GET /users` (base URL `https://{{credentials.domain}}.talentlms.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

