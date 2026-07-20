# Timelink: Get User

Retrieves a user from the Timelink workspace.

```
GET https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timelink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-user?connectionId=$CONNECTION_ID&id=01ABC..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "01ABC..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | The Timelink user ID. Example: `01ABC...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "admin": 1,
      "appData": {},
      "color": "string",
      "companyId": "string",
      "createdAt": "string",
      "electronVersion": {},
      "email": "ava@example.com",
      "emailVerifiedAt": "ava@example.com",
      "extFields": {},
      "extToolId": {},
      "favorites": {},
      "firstName": "Ava",
      "frontendVersion": "string",
      "fullName": "Ava Chen",
      "hasInvitation": 1,
      "id": "string",
      "imageId": {},
      "invitation": {},
      "language": "string",
      "lastName": "Chen",
      "lastSync": {},
      "lastUsed": {},
      "needsInitialPassword": true,
      "settings": {},
      "syncActiveState": {},
      "timezone": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `admin` | number |  |
| `appData` | object |  |
| `color` | string |  |
| `companyId` | string |  |
| `createdAt` | string |  |
| `electronVersion` | object |  |
| `email` | string |  |
| `emailVerifiedAt` | string |  |
| `extFields` | object |  |
| `extToolId` | object |  |
| `favorites` | object |  |
| `firstName` | string |  |
| `frontendVersion` | string |  |
| `fullName` | string |  |
| `hasInvitation` | number |  |
| `id` | string |  |
| `imageId` | object |  |
| `invitation` | object |  |
| `language` | string |  |
| `lastName` | string |  |
| `lastSync` | object |  |
| `lastUsed` | object |  |
| `needsInitialPassword` | boolean |  |
| `settings` | object |  |
| `syncActiveState` | object |  |
| `timezone` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Timelink API, this operation is `GET /users/:id` (base URL `https://api.timelink.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

