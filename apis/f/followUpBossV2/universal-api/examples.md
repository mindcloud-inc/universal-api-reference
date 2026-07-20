# Follow Up Boss Universal API Examples

These examples use the MindCloud API key and Follow Up Boss connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Follow Up Boss.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-current-user?${params}`, {
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
      "account": 1,
      "algoliaAppId": "string",
      "algoliaKey": "string",
      "beta": true,
      "betaOnly": true,
      "callingBehavior": "string",
      "callingEnabled": true,
      "callingPhoneNumberCanText": true,
      "canCreateApiKeys": true,
      "canExport": true,
      "capabilities": {},
      "connectedEmail": {},
      "created": "string",
      "email": "ava@example.com",
      "emailConnectivity": {},
      "features": [
        "string"
      ],
      "firstName": "Ava",
      "fuid": "string",
      "id": 1,
      "isOwner": true,
      "lastName": "Chen",
      "leadEmailAddress": "ava@example.com",
      "name": "Ava Chen",
      "notifyAboutAllLeads": true,
      "notifyBy": [
        "string"
      ],
      "outboundNumber": "string",
      "phone": "string",
      "picture": {},
      "rawSignature": "string",
      "role": "string",
      "shareAppointments": true,
      "shareEmails": true,
      "signature": "string",
      "teamIds": [
        1
      ],
      "teamLeaderOf": [
        1
      ],
      "teamMember": {},
      "textingEnabled": true,
      "timeZone": "string",
      "typesenseEndpoints": [
        "string"
      ],
      "typesenseKey": "string",
      "unreadConversationCount": 1,
      "updated": "string",
      "vcard": {},
      "version": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/followUpBossV2/latest/actions/get-current-user).

## Create Appointment

Creates a new appointment in Follow Up Boss.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/create-appointment', {
  method: 'POST',
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

Example response:

```json
{
  "success": true,
  "data": [
    {
      "allDay": true,
      "created": "2026-05-07T12:00:00.000Z",
      "createdById": 1,
      "description": "string",
      "detailsVisible": true,
      "end": "2026-05-07T12:00:00.000Z",
      "externalCalendarId": "string",
      "externalEventLink": "https://example.com",
      "id": 1,
      "invitees": [
        {}
      ],
      "isDeletable": true,
      "isEditable": true,
      "location": "string",
      "originFub": true,
      "outcome": "string",
      "outcomeId": 1,
      "start": "2026-05-07T12:00:00.000Z",
      "timezone": "string",
      "title": "string",
      "type": "string",
      "typeId": 1,
      "updated": "2026-05-07T12:00:00.000Z",
      "updatedById": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Appointment action reference](actions/create-appointment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/followUpBossV2/latest/actions/create-appointment).
