# CalendarHero: Update Work Location

Updates a work location in CalendarHero.

```
PUT https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/update-work-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CalendarHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/update-work-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/update-work-location', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "associatedOrgId": "string",
      "avatar": "string",
      "branding": {},
      "collaborators": [
        "string"
      ],
      "country": "string",
      "currency": "string",
      "dateAdded": "string",
      "dateLastLogin": "string",
      "datePlanChanged": "string",
      "dateUpdated": "string",
      "directories": {},
      "email": "ava@example.com",
      "emailFooter": "ava@example.com",
      "extraEmails": [
        "ava@example.com"
      ],
      "hideAutomatedAssistant": true,
      "hideNegativeWhoIs": true,
      "inactiveUntilDate": "string",
      "language": "string",
      "location": {},
      "logoUrl": "https://example.com",
      "managed": {},
      "meeting": {},
      "messaging": [
        "string"
      ],
      "name": "Ava Chen",
      "orgId": "string",
      "password": "string",
      "plan": "string",
      "preferredNotificationIndex": 1,
      "preferredNotificationType": "string",
      "restrictedApps": [
        "string"
      ],
      "showcontact": {},
      "stats": {},
      "tags": [
        "string"
      ],
      "telephones": [
        "string"
      ],
      "templates": {},
      "timezone": "string",
      "vendastaLegacyUserId": "string",
      "vendastaTopNavUrl": "https://example.com",
      "vendastaUserId": "string",
      "weather": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `associatedOrgId` | string |  |
| `avatar` | string |  |
| `branding` | object |  |
| `collaborators` | array<string> |  |
| `country` | string |  |
| `currency` | string |  |
| `dateAdded` | string |  |
| `dateLastLogin` | string |  |
| `datePlanChanged` | string |  |
| `dateUpdated` | string |  |
| `directories` | object |  |
| `email` | string |  |
| `emailFooter` | string |  |
| `extraEmails` | array<string> |  |
| `hideAutomatedAssistant` | boolean |  |
| `hideNegativeWhoIs` | boolean |  |
| `inactiveUntilDate` | string |  |
| `language` | string |  |
| `location` | object |  |
| `logoUrl` | string |  |
| `managed` | object |  |
| `meeting` | object |  |
| `messaging` | array<string> |  |
| `name` | string |  |
| `orgId` | string |  |
| `password` | string |  |
| `plan` | string |  |
| `preferredNotificationIndex` | number |  |
| `preferredNotificationType` | string |  |
| `restrictedApps` | array<string> |  |
| `showcontact` | object |  |
| `stats` | object |  |
| `tags` | array<string> |  |
| `telephones` | array<string> |  |
| `templates` | object |  |
| `timezone` | string |  |
| `vendastaLegacyUserId` | string |  |
| `vendastaTopNavUrl` | string |  |
| `vendastaUserId` | string |  |
| `weather` | object |  |

## Native endpoint

Through the native CalendarHero API, this operation is `PUT /user/settings/worklocation` (base URL `https://api.calendarhero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-work-location.md) for the provider-specific parameters and requirements.

