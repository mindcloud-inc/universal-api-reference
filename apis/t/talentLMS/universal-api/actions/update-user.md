# TalentLMS: Update User

Updates an existing user in TalentLMS.

```
PUT https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Numeric user ID. |
| `name` | string | no | Updated first name. |
| `surname` | string | no | Updated last name. |
| `login` | string | no | Updated login username. |
| `email` | string | no | Updated email address. |
| `description` | string | no | Updated user description. |
| `timezone` | string | no | Updated user timezone. |
| `locale` | list | no | Updated user locale. One of: `ar-AE`, `az-AZ`, `bs-BA`, `ca-ES`, `cs-CZ`, `da-DK`, `de-DE`, `el-GR`, `en-US`, `es-ES`, `et-EE`, `fa-IR`, `fi-FI`, `fr-FR`, `he-IL`, `hi-IN`, `hr-HR`, `hu-HU`, `hy-AM`, `id-ID`, `is-IS`, `it-IT`, `ja-JP`, `ka-GE`, `ko-KR`, `lt-LT`, `lv-LV`, `mn-MN`, `ms-MY`, `nb-NO`, `nl-NL`, `pl-PL`, `pt-BR`, `pt-PT`, `ro-RO`, `ru-RU`, `sk-SK`, `sl-SI`, `sr-RS`, `sv-SE`, `th-TH`, `tr-TR`, `uk-UA`, `vi-VN`, `zh-CN`, `zh-TW`. |
| `emailNotifications` | boolean | no | Enable or disable email notifications. |
| `userTypeId` | number | no | Updated user type id. |
| `status` | string | yes | User status (for example, active). |
| `deactivationDate` | string | no | Updated deactivation date. |
| `currentPassword` | string | no | Current password for password change. |
| `password` | string | no | Updated user password. |
| `credits` | number | no | Updated user credits. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableTypes": [
        {}
      ],
      "avatar": {},
      "credits": 1,
      "customFields": [
        {}
      ],
      "deactivationDate": "string",
      "description": "string",
      "email": "ava@example.com",
      "emailNotifications": true,
      "id": 1,
      "locale": "string",
      "login": "string",
      "name": "Ava Chen",
      "status": "string",
      "surname": "Ava Chen",
      "timezone": "string",
      "userType": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableTypes` | array<object> |  |
| `avatar` | object |  |
| `credits` | number |  |
| `customFields` | array<object> |  |
| `deactivationDate` | string |  |
| `description` | string |  |
| `email` | string |  |
| `emailNotifications` | boolean |  |
| `id` | number |  |
| `locale` | string |  |
| `login` | string |  |
| `name` | string |  |
| `status` | string |  |
| `surname` | string |  |
| `timezone` | string |  |
| `userType` | object |  |

## Native endpoint

Through the native TalentLMS API, this operation is `PATCH /users/:id` (base URL `https://{{credentials.domain}}.talentlms.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

