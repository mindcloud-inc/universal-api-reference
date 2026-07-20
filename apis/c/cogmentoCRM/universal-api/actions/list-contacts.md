# Cogmento CRM: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cogmento CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/list-contacts?${params}`, {
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
      "auxId": "string",
      "auxSource": "string",
      "auxSourceName": "Ava Chen",
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
      "description": "string",
      "doNotCall": true,
      "doNotEmail": true,
      "doNotText": true,
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
      "lastCall": "string",
      "lastEvent": "string",
      "lastModified": "string",
      "lastName": "Chen",
      "localTime": "string",
      "middleName": "Ava Chen",
      "name": "Ava Chen",
      "private": true,
      "rating": 1,
      "tags": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "templateId": "string",
      "timezone": "string"
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
| `auxId` | string |  |
| `auxSource` | string |  |
| `auxSourceName` | string |  |
| `channels` | array<object> |  |
| `company` | object |  |
| `createdAt` | string |  |
| `createdBy.email` | string |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdBy.notificationOptIn` | boolean |  |
| `description` | string |  |
| `doNotCall` | boolean |  |
| `doNotEmail` | boolean |  |
| `doNotText` | boolean |  |
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
| `lastCall` | string |  |
| `lastEvent` | string |  |
| `lastModified` | string |  |
| `lastName` | string |  |
| `localTime` | string |  |
| `middleName` | string |  |
| `name` | string |  |
| `private` | boolean |  |
| `rating` | number |  |
| `tags` | array<object> |  |
| `tags[].id` | string |  |
| `tags[].name` | string |  |
| `templateId` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Cogmento CRM API, this operation is `GET /contacts/` (base URL `https://api.freecrm.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

