# Zammad: Get Current User

Retrieves the current user from Zammad.

```
GET https://connect.mindcloud.co/v1/universal/zammad/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zammad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zammad/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zammad/latest/actions/get-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "address": {},
      "city": "string",
      "country": "string",
      "createdAt": "string",
      "createdById": 1,
      "department": {},
      "email": "ava@example.com",
      "fax": "string",
      "firstname": "Ava",
      "groupIds": {
        "1": [
          "string"
        ]
      },
      "id": 1,
      "image": {},
      "imageSource": {},
      "lastLogin": "string",
      "lastname": "Chen",
      "login": "string",
      "loginFailed": 1,
      "mobile": "string",
      "note": "string",
      "organizationId": 1,
      "outOfOffice": true,
      "outOfOfficeEndAt": {},
      "outOfOfficeReplacementId": {},
      "outOfOfficeStartAt": {},
      "phone": "string",
      "preferences": {
        "intro": true,
        "keyboardShortcutsClues": true,
        "locale": "string",
        "notificationConfig": {
          "matrix": {
            "create": {
              "channel": {
                "email": true,
                "online": true
              },
              "criteria": {
                "no": true,
                "ownedByMe": true,
                "ownedByNobody": true,
                "subscribed": true
              }
            },
            "escalation": {
              "channel": {
                "email": true,
                "online": true
              },
              "criteria": {
                "no": true,
                "ownedByMe": true,
                "ownedByNobody": true,
                "subscribed": true
              }
            },
            "reminderReached": {
              "channel": {
                "email": true,
                "online": true
              },
              "criteria": {
                "no": true,
                "ownedByMe": true,
                "ownedByNobody": true,
                "subscribed": true
              }
            },
            "update": {
              "channel": {
                "email": true,
                "online": true
              },
              "criteria": {
                "no": true,
                "ownedByMe": true,
                "ownedByNobody": true,
                "subscribed": true
              }
            }
          }
        }
      },
      "roleIds": [
        1
      ],
      "source": {},
      "street": "string",
      "updatedAt": "string",
      "updatedById": 1,
      "verified": true,
      "vip": true,
      "web": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `address` | object |  |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | string |  |
| `createdById` | number |  |
| `department` | object |  |
| `email` | string |  |
| `fax` | string |  |
| `firstname` | string |  |
| `groupIds.1[]` | string |  |
| `id` | number |  |
| `image` | object |  |
| `imageSource` | object |  |
| `lastLogin` | string |  |
| `lastname` | string |  |
| `login` | string |  |
| `loginFailed` | number |  |
| `mobile` | string |  |
| `note` | string |  |
| `organizationId` | number |  |
| `outOfOffice` | boolean |  |
| `outOfOfficeEndAt` | object |  |
| `outOfOfficeReplacementId` | object |  |
| `outOfOfficeStartAt` | object |  |
| `phone` | string |  |
| `preferences.intro` | boolean |  |
| `preferences.keyboardShortcutsClues` | boolean |  |
| `preferences.locale` | string |  |
| `preferences.notificationConfig.matrix.create.channel.email` | boolean |  |
| `preferences.notificationConfig.matrix.create.channel.online` | boolean |  |
| `preferences.notificationConfig.matrix.create.criteria.no` | boolean |  |
| `preferences.notificationConfig.matrix.create.criteria.ownedByMe` | boolean |  |
| `preferences.notificationConfig.matrix.create.criteria.ownedByNobody` | boolean |  |
| `preferences.notificationConfig.matrix.create.criteria.subscribed` | boolean |  |
| `preferences.notificationConfig.matrix.escalation.channel.email` | boolean |  |
| `preferences.notificationConfig.matrix.escalation.channel.online` | boolean |  |
| `preferences.notificationConfig.matrix.escalation.criteria.no` | boolean |  |
| `preferences.notificationConfig.matrix.escalation.criteria.ownedByMe` | boolean |  |
| `preferences.notificationConfig.matrix.escalation.criteria.ownedByNobody` | boolean |  |
| `preferences.notificationConfig.matrix.escalation.criteria.subscribed` | boolean |  |
| `preferences.notificationConfig.matrix.reminderReached.channel.email` | boolean |  |
| `preferences.notificationConfig.matrix.reminderReached.channel.online` | boolean |  |
| `preferences.notificationConfig.matrix.reminderReached.criteria.no` | boolean |  |
| `preferences.notificationConfig.matrix.reminderReached.criteria.ownedByMe` | boolean |  |
| `preferences.notificationConfig.matrix.reminderReached.criteria.ownedByNobody` | boolean |  |
| `preferences.notificationConfig.matrix.reminderReached.criteria.subscribed` | boolean |  |
| `preferences.notificationConfig.matrix.update.channel.email` | boolean |  |
| `preferences.notificationConfig.matrix.update.channel.online` | boolean |  |
| `preferences.notificationConfig.matrix.update.criteria.no` | boolean |  |
| `preferences.notificationConfig.matrix.update.criteria.ownedByMe` | boolean |  |
| `preferences.notificationConfig.matrix.update.criteria.ownedByNobody` | boolean |  |
| `preferences.notificationConfig.matrix.update.criteria.subscribed` | boolean |  |
| `roleIds[]` | number |  |
| `source` | object |  |
| `street` | string |  |
| `updatedAt` | string |  |
| `updatedById` | number |  |
| `verified` | boolean |  |
| `vip` | boolean |  |
| `web` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native Zammad API, this operation is `GET /users/me` (base URL `{{credentials.baseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

