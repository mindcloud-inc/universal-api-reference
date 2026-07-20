# CalendarHero Universal API Examples

These examples use the MindCloud API key and CalendarHero connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User

Retrieves a user from CalendarHero.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/get-user?${params}`, {
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

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/calendarHero/latest/actions/get-user).

## Create Contact

Creates a contact in CalendarHero.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/create-contact', {
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
  "data": [],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/calendarHero/latest/actions/create-contact).
