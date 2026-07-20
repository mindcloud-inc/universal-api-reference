# Appwrite: Create team membership

Creates a new team membership in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/teams-create-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/teams-create-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "roles[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/teams-create-membership', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "roles[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roles` | string | no | Array of strings. Use this param to set the user roles in the team. A role can be any string. Learn more about [roles and permissions](https://appwrite.io/docs/permissions). Maximum of 100 roles are allowed, each 32 characters long. |
| `teamId` | string | yes | Team ID. |
| `email` | string | no | Email of the new team member. |
| `userId` | string | no | ID of the user to be added to a team. |
| `phone` | string | no | Phone number. Format this number with a leading '+' and a country code, e.g., +16175551212. |
| `roles[]` | array<string> | yes | Array of strings. Use this param to set the user roles in the team. A role can be any string. Learn more about [roles and permissions](https://appwrite.io/docs/permissions). Maximum of 100 roles are allowed, each 32 characters long. |
| `url` | string | no | URL to redirect the user back to your app from the invitation email. This parameter is not required when an API key is supplied. Only URLs from hostnames in your project platform list are allowed. This requirement helps to prevent an [open redirect](https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html) attack against your project API. |
| `name` | string | no | Name of the new team member. Max length: 128 chars. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "confirm": true,
      "invited": "string",
      "joined": "string",
      "mfa": true,
      "roles": [
        "string"
      ],
      "teamId": "string",
      "teamName": "Ava Chen",
      "userEmail": "ava@example.com",
      "userId": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Membership creation date in ISO 8601 format. |
| `$id` | string | Membership ID. |
| `$updatedAt` | string | Membership update date in ISO 8601 format. |
| `confirm` | boolean | User confirmation status, true if the user has joined the team or false otherwise. |
| `invited` | string | Date, the user has been invited to join the team in ISO 8601 format. |
| `joined` | string | Date, the user has accepted the invitation to join the team in ISO 8601 format. |
| `mfa` | boolean | Multi factor authentication status, true if the user has MFA enabled or false otherwise. Hide this attribute by toggling membership privacy in the Console. |
| `roles` | array<string> | User list of roles |
| `teamId` | string | Team ID. |
| `teamName` | string | Team name. |
| `userEmail` | string | User email address. Hide this attribute by toggling membership privacy in the Console. |
| `userId` | string | User ID. |
| `userName` | string | User name. Hide this attribute by toggling membership privacy in the Console. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /teams/{teamId}/memberships` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/teams-create-membership.md) for the provider-specific parameters and requirements.

