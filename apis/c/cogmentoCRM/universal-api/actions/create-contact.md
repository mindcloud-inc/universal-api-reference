# Cogmento CRM: Create Contact



```
POST https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cogmento CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | First name of the contact. |
| `lastName` | string | yes | Last name of the contact. |
| `description` | string | no | Description of the contact. |
| `tags[]` | array<string> | no | Tags associated with the contact. Accepts multiple values as an array. |
| `doNotCall` | boolean | no | Set true to mark the contact as do not call. |
| `doNotText` | boolean | no | Set true to mark the contact as do not text. |
| `doNotEmail` | boolean | no | Set true to mark the contact as do not email. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channels[]` | array<object> | no | Contact channels array, such as email or phone channel objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": {
        "private": true
      },
      "accountId": "string",
      "acl": [
        {}
      ],
      "addresses": [
        {}
      ],
      "alerts": [
        {}
      ],
      "auxId": "string",
      "auxSource": "string",
      "auxSourceName": "Ava Chen",
      "calls": [
        {}
      ],
      "campaigns": [
        {}
      ],
      "cases": [
        {}
      ],
      "channels": [
        {}
      ],
      "company": {},
      "createdAt": "string",
      "createdBy": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "notificationOptIn": true
      },
      "credentials": [
        {}
      ],
      "deals": [
        {}
      ],
      "description": "string",
      "documents": [
        {}
      ],
      "doNotCall": true,
      "doNotEmail": true,
      "doNotText": true,
      "events": [
        {}
      ],
      "firstName": "Ava",
      "flags": {
        "callAssigned": true,
        "caseAssigned": true,
        "emailReceived": true,
        "eventAssigned": true,
        "new": true,
        "taskAssigned": true,
        "updated": true
      },
      "fullName": "Ava Chen",
      "id": "string",
      "invoices": [
        {}
      ],
      "lastCall": "string",
      "lastEvent": "string",
      "lastModified": "string",
      "lastName": "Chen",
      "localTime": "string",
      "middleName": "Ava Chen",
      "name": "Ava Chen",
      "notes": [
        {}
      ],
      "private": true,
      "rating": 1,
      "sms": [
        {}
      ],
      "submissions": [
        {}
      ],
      "tags": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "tasks": [
        {}
      ],
      "templateId": "string",
      "timezone": "string",
      "whatsapp": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access.private` | boolean |  |
| `accountId` | string |  |
| `acl` | array<object> |  |
| `addresses` | array<object> |  |
| `alerts` | array<object> |  |
| `auxId` | string |  |
| `auxSource` | string |  |
| `auxSourceName` | string |  |
| `calls` | array<object> |  |
| `campaigns` | array<object> |  |
| `cases` | array<object> |  |
| `channels` | array<object> |  |
| `company` | object |  |
| `createdAt` | string |  |
| `createdBy.email` | string |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdBy.notificationOptIn` | boolean |  |
| `credentials` | array<object> |  |
| `deals` | array<object> |  |
| `description` | string |  |
| `documents` | array<object> |  |
| `doNotCall` | boolean |  |
| `doNotEmail` | boolean |  |
| `doNotText` | boolean |  |
| `events` | array<object> |  |
| `firstName` | string |  |
| `flags.callAssigned` | boolean |  |
| `flags.caseAssigned` | boolean |  |
| `flags.emailReceived` | boolean |  |
| `flags.eventAssigned` | boolean |  |
| `flags.new` | boolean |  |
| `flags.taskAssigned` | boolean |  |
| `flags.updated` | boolean |  |
| `fullName` | string |  |
| `id` | string |  |
| `invoices` | array<object> |  |
| `lastCall` | string |  |
| `lastEvent` | string |  |
| `lastModified` | string |  |
| `lastName` | string |  |
| `localTime` | string |  |
| `middleName` | string |  |
| `name` | string |  |
| `notes` | array<object> |  |
| `private` | boolean |  |
| `rating` | number |  |
| `sms` | array<object> |  |
| `submissions` | array<object> |  |
| `tags` | array<object> |  |
| `tags[].id` | string |  |
| `tags[].name` | string |  |
| `tasks` | array<object> |  |
| `templateId` | string |  |
| `timezone` | string |  |
| `whatsapp` | array<object> |  |

## Native endpoint

Through the native Cogmento CRM API, this operation is `POST /contacts/` (base URL `https://api.freecrm.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

