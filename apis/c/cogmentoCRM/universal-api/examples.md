# Cogmento CRM Universal API Examples

These examples use the MindCloud API key and Cogmento CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/get-current-user?${params}`, {
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
      "accountId": "string",
      "accountOwner": true,
      "createdAt": "string",
      "email": "ava@example.com",
      "facebookAuth": true,
      "firstName": "Ava",
      "google": true,
      "hasDocusign": true,
      "hasTemplates": true,
      "id": "string",
      "lastName": "Chen",
      "linkedinAuth": true,
      "oneSignalIds": [
        "string"
      ],
      "phoneVerified": true,
      "quickbooks": true,
      "security": {
        "groups": [
          "string"
        ],
        "permissions": [
          "string"
        ],
        "ssi": true
      },
      "settings": {
        "locale": "string"
      },
      "telephony": true,
      "timezone": "string",
      "twilioNumbers": [
        "string"
      ],
      "verifiedForCalls": true
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cogmentoCRM/latest/actions/get-current-user).

## Create Contact



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

Example response:

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

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cogmentoCRM/latest/actions/create-contact).
