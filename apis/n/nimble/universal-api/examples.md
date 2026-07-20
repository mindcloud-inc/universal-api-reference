# Nimble Universal API Examples

These examples use the MindCloud API key and Nimble connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the authenticated user from Nimble.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nimble/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nimble/latest/actions/get-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "companySize": 1,
      "email": "ava@example.com",
      "name": "Ava Chen",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nimble/latest/actions/get-current-user).

## Assign Tags to Contact

Updates tags for a contact in Nimble.

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

Example response:

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

See the full [Assign Tags to Contact action reference](actions/assign-tags-to-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nimble/latest/actions/assign-tags-to-contact).
