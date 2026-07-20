# Teamgate Universal API Examples

These examples use the MindCloud API key and Teamgate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from Teamgate.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-users?${params}`, {
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
      "accountUrl": "https://example.com",
      "created": {
        "time": "string"
      },
      "currencies": [
        {
          "fullRate": "string",
          "iso": "string",
          "name": "Ava Chen",
          "rate": "string",
          "symbol": "string"
        }
      ],
      "defaultCurrency": "string",
      "email": "ava@example.com",
      "id": 1,
      "isActive": "string",
      "language": {
        "code": "string",
        "name": "Ava Chen"
      },
      "lastLogin": {
        "time": "string"
      },
      "locale": "string",
      "name": "Ava Chen",
      "permissions": {
        "companies": [
          {}
        ],
        "deals": [
          {}
        ],
        "events": [
          {}
        ],
        "leads": [
          {}
        ],
        "people": [
          {}
        ],
        "settingsUsersGroups": [
          {}
        ]
      },
      "picture": {
        "large": "string",
        "medium": "string",
        "small": "string"
      },
      "role": "string",
      "surname": "Ava Chen",
      "timeZone": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teamgate/latest/actions/list-users).

## Create Appointment

Creates a new appointment in Teamgate.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Kickoff meeting"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Kickoff meeting"
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
      "allDay": "string",
      "canEdit": "string",
      "canView": "string",
      "companies": [
        {}
      ],
      "completed": {},
      "created": {},
      "deals": [
        {}
      ],
      "end": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isDeleted": "string",
      "isSecret": "string",
      "name": "Ava Chen",
      "owner": {},
      "start": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "type": "string",
      "updated": {},
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Appointment action reference](actions/create-appointment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teamgate/latest/actions/create-appointment).
