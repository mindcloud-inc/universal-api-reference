# Appwrite: Get team membership

Retrieves the team membership from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/teams-get-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/teams-get-membership?connectionId=$CONNECTION_ID&teamId=string&membershipId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "membershipId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/teams-get-membership?${params}`, {
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
| `teamId` | string | yes | Team ID. |
| `membershipId` | string | yes | Membership ID. |

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

Through the native Appwrite API, this operation is `GET /teams/{teamId}/memberships/{membershipId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/teams-get-membership.md) for the provider-specific parameters and requirements.

