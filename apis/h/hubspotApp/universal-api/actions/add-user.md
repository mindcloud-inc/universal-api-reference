# HubSpot: Add User

Creates a new user in HubSpot.

```
POST https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/add-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/add-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "sendWelcomeEmail": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/add-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "sendWelcomeEmail": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address for the new HubSpot user. |
| `sendWelcomeEmail` | boolean | yes | Whether HubSpot should email the user a welcome message. |
| `firstName` | string | no | First name for the user. |
| `lastName` | string | no | Last name for the user. |
| `primaryTeamId` | string | no | Primary HubSpot team ID for the user. |
| `roleId` | string | no | HubSpot role ID to assign to the user. |
| `secondaryTeamIds[]` | array<string> | no | Additional HubSpot team IDs for the user. |

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
| `id` | string | HubSpot user ID. |
| `lastName` | string | The user's last name. |
| `primaryTeamId` | string | Primary HubSpot team ID. |
| `roleIds` | array<string> | Assigned HubSpot role IDs. |
| `secondaryTeamIds` | array<string> | Additional HubSpot team IDs. |
| `superAdmin` | boolean | Whether the user is a super admin. |

## Native endpoint

Through the native HubSpot API, this operation is `POST settings/v3/users/` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user.md) for the provider-specific parameters and requirements.

