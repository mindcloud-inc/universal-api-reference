# Dialpad: List Users

Retrieves company user records from Dialpad.

```
GET https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-users?${params}`, {
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
| `cursor` | string | no | A token used to return the next page of a previous request. Use the cursor provided in the previous response. |
| `state` | string | no | Filter results by the specified user state. |
| `company_admin` | boolean | no | If provided, filter results to company admins or non-company admins. |
| `email` | string | no | The user's email. |
| `number` | string | no | The user's phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "emails": [
        "ava@example.com"
      ],
      "firstName": "Ava",
      "id": "string",
      "imageUrl": "https://example.com",
      "internationalDialingEnabled": true,
      "isAdmin": true,
      "isSuperAdmin": true,
      "lastName": "Chen",
      "license": "string",
      "officeId": "string",
      "phoneNumbers": [
        "string"
      ],
      "state": "string",
      "timezone": "string",
      "voicemail": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `emails` | array<string> |  |
| `firstName` | string |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `internationalDialingEnabled` | boolean |  |
| `isAdmin` | boolean |  |
| `isSuperAdmin` | boolean |  |
| `lastName` | string |  |
| `license` | string |  |
| `officeId` | string |  |
| `phoneNumbers` | array<string> |  |
| `state` | string |  |
| `timezone` | string |  |
| `voicemail` | object |  |

## Native endpoint

Through the native Dialpad API, this operation is `GET /users` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

