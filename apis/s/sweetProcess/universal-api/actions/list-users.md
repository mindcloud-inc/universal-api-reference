# SweetProcess: List Users

Retrieves users from SweetProcess.

```
GET https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SweetProcess `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/list-users?${params}`, {
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
| `id` | number | no | Filter users by the numeric SweetProcess user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "email": "ava@example.com",
      "htmlUrl": "https://example.com",
      "id": 1,
      "isAccountOnly": true,
      "isActive": true,
      "isBillingAdmin": true,
      "isDeleted": true,
      "isEmailVerified": true,
      "isManager": true,
      "isSuperManager": true,
      "isSuperTeammate": true,
      "name": "Ava Chen",
      "teamMemberships": [
        {}
      ],
      "teams": [
        {}
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | The SweetProcess content type for the record, for example user. |
| `email` | string | The user's primary email address. |
| `htmlUrl` | string | The SweetProcess web URL for the user. |
| `id` | number | The numeric SweetProcess user ID. |
| `isAccountOnly` | boolean | Whether the user exists only at the account level. |
| `isActive` | boolean | Whether the user is active in SweetProcess. |
| `isBillingAdmin` | boolean | Whether the user is a billing administrator. |
| `isDeleted` | boolean | Whether the user has been deleted. |
| `isEmailVerified` | boolean | Whether the user's email is verified. |
| `isManager` | boolean | Whether the user is a manager. |
| `isSuperManager` | boolean | Whether the user is a super manager. |
| `isSuperTeammate` | boolean | Whether the user is a super teammate. |
| `name` | string | The user's display name. |
| `teamMemberships` | array<object> | The user's team membership objects. |
| `teams` | array<object> | The teams currently associated with the user. |
| `url` | string | The API URL for the SweetProcess user. |

## Native endpoint

Through the native SweetProcess API, this operation is `GET /users/` (base URL `https://www.sweetprocess.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

