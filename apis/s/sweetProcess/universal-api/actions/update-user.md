# SweetProcess: Update User

Updates an existing teammate in SweetProcess.

```
PUT https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SweetProcess `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The numeric SweetProcess user ID. |
| `name` | string | no | The teammate's display name. |
| `email` | string | no | The teammate's email address. Example: `new.email@example.com`. |
| `isSuperManager` | boolean | no | Whether the teammate has super manager access. |
| `isSuperTeammate` | boolean | no | Whether the teammate has super teammate access. |
| `isBillingAdmin` | boolean | no | Whether the teammate has billing admin access. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarImage": "string",
      "canEdit": true,
      "contentType": "string",
      "email": "ava@example.com",
      "emailaddresses": [
        {}
      ],
      "emailstatus": "ava@example.com",
      "htmlUrl": "https://example.com",
      "id": 1,
      "isAccountOnly": true,
      "isActive": true,
      "isBillingAdmin": true,
      "isDeleted": true,
      "isEmailVerified": true,
      "isGuestUntil": "2026-05-07T12:00:00.000Z",
      "isManager": true,
      "isSamlAccount": true,
      "isSuperManager": true,
      "isSuperTeammate": true,
      "isTwoFactor": true,
      "name": "Ava Chen",
      "teamMemberships": [
        {}
      ],
      "teams": [
        {}
      ],
      "timezone": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarImage` | string | The user's avatar image URL, when present. |
| `canEdit` | boolean | Whether the current actor can edit the user. |
| `contentType` | string | The SweetProcess content type for the record, for example user. |
| `email` | string | The user's primary email address. |
| `emailaddresses` | array<object> | The user's email address records. |
| `emailstatus` | string | The current email delivery status, when available. |
| `htmlUrl` | string | The SweetProcess web URL for the user. |
| `id` | number | The numeric SweetProcess user ID. |
| `isAccountOnly` | boolean | Whether the user exists only at the account level. |
| `isActive` | boolean | Whether the user is active in SweetProcess. |
| `isBillingAdmin` | boolean | Whether the user is a billing administrator. |
| `isDeleted` | boolean | Whether the user has been deleted. |
| `isEmailVerified` | boolean | Whether the user's email is verified. |
| `isGuestUntil` | date | When a guest user's access ends, if applicable. |
| `isManager` | boolean | Whether the user is a manager. |
| `isSamlAccount` | boolean | Whether the user is a SAML account. |
| `isSuperManager` | boolean | Whether the user is a super manager. |
| `isSuperTeammate` | boolean | Whether the user is a super teammate. |
| `isTwoFactor` | boolean | Whether two-factor authentication is enabled. |
| `name` | string | The user's display name. |
| `teamMemberships` | array<object> | The user's team membership objects. |
| `teams` | array<object> | The teams currently associated with the user. |
| `timezone` | string | The user's configured time zone. |
| `url` | string | The API URL for the SweetProcess user. |

## Native endpoint

Through the native SweetProcess API, this operation is `PATCH /users/:id/` (base URL `https://www.sweetprocess.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

