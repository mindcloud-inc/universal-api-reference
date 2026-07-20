# HubSpot: List Users

Retrieves users from HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-users?${params}`, {
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "primaryTeamId": "string",
      "roleIds": [
        "string"
      ],
      "secondaryTeamIds": [
        "string"
      ],
      "superAdmin": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | The user's email address. |
| `firstName` | string | The user's first name. |
| `id` | string | The HubSpot user ID. |
| `lastName` | string | The user's last name. |
| `primaryTeamId` | string | The user's primary team ID. |
| `roleIds` | array<string> | Assigned HubSpot role IDs. |
| `secondaryTeamIds` | array<string> | Additional team IDs for the user. |
| `superAdmin` | boolean | Whether the user is a super admin. |

## Native endpoint

Through the native HubSpot API, this operation is `GET settings/v3/users` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

