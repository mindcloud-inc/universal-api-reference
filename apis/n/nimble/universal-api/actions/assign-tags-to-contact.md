# Nimble: Assign Tags to Contact

Updates tags for a contact in Nimble.

```
PUT https://connect.mindcloud.co/v1/universal/nimble/latest/actions/assign-tags-to-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nimble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nimble/latest/actions/assign-tags-to-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "tags[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nimble/latest/actions/assign-tags-to-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "tags[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | Nimble contact_id path parameter. |
| `tags[]` | array<string> | yes |  |

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
          {}
        ]
      ],
      "fields": {
        "address": [
          [
            {}
          ]
        ],
        "contactEmployment": [
          [
            {}
          ]
        ],
        "description": [
          [
            {}
          ]
        ],
        "discoveredEducation": [
          [
            {}
          ]
        ],
        "email": [
          [
            {}
          ]
        ],
        "facebook": [
          [
            {}
          ]
        ],
        "firstName": [
          [
            {}
          ]
        ],
        "lastName": [
          [
            {}
          ]
        ],
        "linkedin": [
          [
            {}
          ]
        ],
        "parentCompany": [
          [
            {}
          ]
        ],
        "title": [
          [
            {}
          ]
        ],
        "twitter": [
          [
            {}
          ]
        ],
        "url": [
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
        [
          {}
        ]
      ],
      "tags2": [
        [
          "string"
        ]
      ],
      "updated": "string",
      "updater": "string"
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
| `employersInfo[]` | array<object> |  |
| `employersInfo[].avatarUrl` | string |  |
| `employersInfo[].companyName` | string |  |
| `employersInfo[].contactId` | string |  |
| `fields` | object |  |
| `fields.address[]` | array<object> |  |
| `fields.address[].isPrimary` | boolean |  |
| `fields.address[].label` | string |  |
| `fields.address[].modifier` | string |  |
| `fields.address[].value` | string |  |
| `fields.contactEmployment[]` | array<object> |  |
| `fields.contactEmployment[].extraValue` | string |  |
| `fields.contactEmployment[].isPrimary` | boolean |  |
| `fields.contactEmployment[].label` | string |  |
| `fields.contactEmployment[].modifier` | string |  |
| `fields.contactEmployment[].value` | string |  |
| `fields.description[]` | array<object> |  |
| `fields.description[].isPrimary` | boolean |  |
| `fields.description[].label` | string |  |
| `fields.description[].modifier` | string |  |
| `fields.description[].value` | string |  |
| `fields.discoveredEducation[]` | array<object> |  |
| `fields.discoveredEducation[].isPrimary` | boolean |  |
| `fields.discoveredEducation[].label` | string |  |
| `fields.discoveredEducation[].modifier` | string |  |
| `fields.discoveredEducation[].value` | string |  |
| `fields.email[]` | array<object> |  |
| `fields.email[].isPrimary` | boolean |  |
| `fields.email[].label` | string |  |
| `fields.email[].modifier` | string |  |
| `fields.email[].value` | string |  |
| `fields.facebook[]` | array<object> |  |
| `fields.facebook[].isPrimary` | boolean |  |
| `fields.facebook[].label` | string |  |
| `fields.facebook[].modifier` | string |  |
| `fields.facebook[].value` | string |  |
| `fields.firstName[]` | array<object> |  |
| `fields.firstName[].isPrimary` | boolean |  |
| `fields.firstName[].label` | string |  |
| `fields.firstName[].modifier` | string |  |
| `fields.firstName[].value` | string |  |
| `fields.lastName[]` | array<object> |  |
| `fields.lastName[].isPrimary` | boolean |  |
| `fields.lastName[].label` | string |  |
| `fields.lastName[].modifier` | string |  |
| `fields.lastName[].value` | string |  |
| `fields.linkedin[]` | array<object> |  |
| `fields.linkedin[].isPrimary` | boolean |  |
| `fields.linkedin[].label` | string |  |
| `fields.linkedin[].modifier` | string |  |
| `fields.linkedin[].value` | string |  |
| `fields.parentCompany[]` | array<object> |  |
| `fields.parentCompany[].extraValue` | string |  |
| `fields.parentCompany[].isPrimary` | boolean |  |
| `fields.parentCompany[].label` | string |  |
| `fields.parentCompany[].modifier` | string |  |
| `fields.parentCompany[].value` | string |  |
| `fields.title[]` | array<object> |  |
| `fields.title[].isPrimary` | boolean |  |
| `fields.title[].label` | string |  |
| `fields.title[].modifier` | string |  |
| `fields.title[].value` | string |  |
| `fields.twitter[]` | array<object> |  |
| `fields.twitter[].isPrimary` | boolean |  |
| `fields.twitter[].label` | string |  |
| `fields.twitter[].modifier` | string |  |
| `fields.twitter[].value` | string |  |
| `fields.url[]` | array<object> |  |
| `fields.url[].isPrimary` | boolean |  |
| `fields.url[].label` | string |  |
| `fields.url[].modifier` | string |  |
| `fields.url[].value` | string |  |
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
| `tags[]` | array<object> |  |
| `tags[].id` | string |  |
| `tags[].tag` | string |  |
| `tags2[]` | array<string> |  |
| `updated` | string |  |
| `updater` | string |  |

## Native endpoint

Through the native Nimble API, this operation is `PUT /api/v1/contacts/:contact_id/tags` (base URL `https://app.nimble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-tags-to-contact.md) for the provider-specific parameters and requirements.

