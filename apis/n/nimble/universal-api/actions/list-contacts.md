# Nimble: List Contacts

Retrieves a filtered list of contacts from Nimble.

```
GET https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nimble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nimble/latest/actions/list-contacts?${params}`, {
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
      "avatarUrl": "https://example.com",
      "children": [
        [
          "string"
        ]
      ],
      "companyLastContacted": {
        "in": {},
        "out": {}
      },
      "contexts": [
        [
          {}
        ]
      ],
      "created": "string",
      "creator": "string",
      "creatorId": "string",
      "employersInfo": [
        [
          "string"
        ]
      ],
      "fields": {
        "companyName": [
          [
            {}
          ]
        ],
        "twitter": [
          [
            {}
          ]
        ]
      },
      "files": {},
      "id": "string",
      "isEditable": true,
      "isImportant": {},
      "lastContacted": {
        "deletionTstamp": {},
        "objectId": {},
        "tstamp": {},
        "type": {},
        "userId": {}
      },
      "lastContactedUser": {},
      "lc": {},
      "notice": {},
      "objectType": "string",
      "ownerId": {},
      "privacy": {
        "edit": {},
        "read": {}
      },
      "recordType": "string",
      "reminder": {},
      "reminders": {},
      "stagesInfo": {},
      "tags": [
        {
          "id": "string",
          "tag": "string"
        }
      ],
      "tags2": [
        "string"
      ],
      "updated": "string",
      "updater": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `children[]` | array<string> |  |
| `companyLastContacted` | object |  |
| `companyLastContacted.in` | object |  |
| `companyLastContacted.out` | object |  |
| `contexts[]` | array<object> |  |
| `contexts[].context` | object |  |
| `contexts[].contextKey` | string |  |
| `created` | string |  |
| `creator` | string |  |
| `creatorId` | string |  |
| `employersInfo[]` | array<string> |  |
| `fields` | object |  |
| `fields.companyName[]` | array<object> |  |
| `fields.companyName[].isPrimary` | boolean |  |
| `fields.companyName[].label` | string |  |
| `fields.companyName[].modifier` | string |  |
| `fields.companyName[].value` | string |  |
| `fields.twitter[]` | array<object> |  |
| `fields.twitter[].isPrimary` | boolean |  |
| `fields.twitter[].label` | string |  |
| `fields.twitter[].modifier` | string |  |
| `fields.twitter[].value` | string |  |
| `files` | object |  |
| `id` | string |  |
| `isEditable` | boolean |  |
| `isImportant` | object |  |
| `lastContacted` | object |  |
| `lastContacted.deletionTstamp` | object |  |
| `lastContacted.objectId` | object |  |
| `lastContacted.tstamp` | object |  |
| `lastContacted.type` | object |  |
| `lastContacted.userId` | object |  |
| `lastContactedUser` | object |  |
| `lc` | object |  |
| `notice` | object |  |
| `objectType` | string |  |
| `ownerId` | object |  |
| `privacy` | object |  |
| `privacy.edit` | object |  |
| `privacy.read` | object |  |
| `recordType` | string |  |
| `reminder` | object |  |
| `reminders` | object |  |
| `stagesInfo` | object |  |
| `tags[]` | string |  |
| `tags[].id` | string |  |
| `tags[].tag` | string |  |
| `tags2[]` | string |  |
| `updated` | string |  |
| `updater` | object |  |

## Native endpoint

Through the native Nimble API, this operation is `GET /api/v1/contacts` (base URL `https://app.nimble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

