# Dialpad: Get User

Retrieves detailed user information from Dialpad.

```
GET https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | The user's id. 'me' can be used if you are using a user level API key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminOfficeIds": [
        "string"
      ],
      "companyId": "string",
      "country": "string",
      "dateActive": "string",
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
      "phoneNumbers": [
        "string"
      ],
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
| `adminOfficeIds[]` | string |  |
| `companyId` | string |  |
| `country` | string |  |
| `dateActive` | string |  |
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
| `phoneNumbers[]` | string |  |
| `remoteService` | string |  |
| `state` | string |  |
| `timezone` | string |  |
| `voicemail.isDefaultVoicemail` | boolean |  |
| `voicemail.name` | string |  |
| `voicemail.voicemailNotificationsEnabled` | boolean |  |

## Native endpoint

Through the native Dialpad API, this operation is `GET /users/:id` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

