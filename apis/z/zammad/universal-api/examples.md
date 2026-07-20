# Zammad Universal API Examples

These examples use the MindCloud API key and Zammad connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Zammad.

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

Example response:

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

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zammad/latest/actions/get-current-user).

## Create Group

Creates a new group in Zammad.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zammad/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MC TEST GROUP"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zammad/latest/actions/create-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MC TEST GROUP"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Group action reference](actions/create-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zammad/latest/actions/create-group).
