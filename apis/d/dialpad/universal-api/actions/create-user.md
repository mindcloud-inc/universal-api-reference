# Dialpad: Create User

Creates a new user in Dialpad.

```
POST https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "office_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "office_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `auto_assign` | boolean | no | If set to true, a number will be automatically assigned. Default: `false`. |
| `email` | string | yes | The user's email. |
| `first_name` | string | no | The user's first name. |
| `last_name` | string | no | The user's last name. |
| `license` | string | no | The user's license type. This affects billing for the user. Default: `talk`. |
| `office_id` | number | yes | The user's office id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "country": "string",
      "dateAdded": "string",
      "displayName": "Ava Chen",
      "doNotDisturb": true,
      "emails": [
        "ava@example.com"
      ],
      "firstName": "Ava",
      "hasRbac": true,
      "id": "string",
      "imageUrl": "https://example.com",
      "internationalDialingEnabled": true,
      "isAdmin": true,
      "isAvailable": true,
      "isOnDuty": true,
      "isOnline": true,
      "isSuperAdmin": true,
      "language": "string",
      "lastName": "Chen",
      "license": "string",
      "muted": true,
      "officeId": "string",
      "onboardingCompleted": true,
      "remoteService": "string",
      "state": "string",
      "timezone": "string",
      "voicemail": {
        "isDefaultVoicemail": true,
        "name": "ava@example.com",
        "voicemailNotificationsEnabled": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `country` | string |  |
| `dateAdded` | string |  |
| `displayName` | string |  |
| `doNotDisturb` | boolean |  |
| `emails[]` | string |  |
| `firstName` | string |  |
| `hasRbac` | boolean |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `internationalDialingEnabled` | boolean |  |
| `isAdmin` | boolean |  |
| `isAvailable` | boolean |  |
| `isOnDuty` | boolean |  |
| `isOnline` | boolean |  |
| `isSuperAdmin` | boolean |  |
| `language` | string |  |
| `lastName` | string |  |
| `license` | string |  |
| `muted` | boolean |  |
| `officeId` | string |  |
| `onboardingCompleted` | boolean |  |
| `remoteService` | string |  |
| `state` | string |  |
| `timezone` | string |  |
| `voicemail.isDefaultVoicemail` | boolean |  |
| `voicemail.name` | string |  |
| `voicemail.voicemailNotificationsEnabled` | boolean |  |

## Native endpoint

Through the native Dialpad API, this operation is `POST /users` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

