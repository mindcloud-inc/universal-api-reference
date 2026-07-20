# Dialpad: Update User

Updates an existing user in Dialpad.

```
PUT https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The user's id. 'me' can be used if you are using a user level API key. |
| `first_name` | string | no | The user's first name. |
| `last_name` | string | no | The user's last name. |
| `emails[]` | array<string> | no | The user's emails. The first email in the list is the user's primary email. |
| `extension` | string | no | The user's new extension number. |
| `job_title` | string | no | The user's job title. |
| `license` | string | no | The user's license type. Changing this affects billing for the user. |
| `office_id` | number | no | The user's office id. |
| `admin_office_ids[]` | array<number> | no | The list of admin office IDs. |
| `phone_numbers[]` | array<string> | no | A list of the phone number(s) assigned to this user. |
| `forwarding_numbers[]` | array<string> | no | A list of phone numbers that should be dialed in addition to the user's Dialpad number(s) upon receiving a call. |
| `international_dialing_enabled` | boolean | no | Whether or not the user is enabled to dial internationally. |
| `is_super_admin` | boolean | no | Whether or not the user is a super admin. |
| `keep_paid_numbers` | boolean | no | Whether or not to keep phone numbers when switching to a support license. Default: `true`. |
| `presence_status` | object | no | The presence status object to update. |
| `state` | string | no | The user's state. |

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

Through the native Dialpad API, this operation is `PATCH /users/:id` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

