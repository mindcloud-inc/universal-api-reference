# Webex Universal API Examples

These examples use the MindCloud API key and Webex connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Own Details

Retrieves your own profile details from Webex.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webex/latest/actions/get-my-own-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webex/latest/actions/get-my-own-details?${params}`, {
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
      "avatar": "https://example.com",
      "created": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "emails": [
        "ava@example.com"
      ],
      "firstName": "Ava",
      "id": "string",
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "licenses": [
        "string"
      ],
      "nickName": "Ava Chen",
      "orgId": "string",
      "phoneNumbers": [
        {}
      ],
      "status": "string",
      "timezone": "string",
      "type": "string",
      "userName": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get My Own Details action reference](actions/get-my-own-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webex/latest/actions/get-my-own-details).

## Create Meeting

Creates a new meeting in Webex.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webex/latest/actions/create-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "MindCloud Test Meeting",
  "start": "2026-04-20T15:00:00Z",
  "end": "2026-04-20T15:30:00Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webex/latest/actions/create-meeting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "MindCloud Test Meeting",
    "start": "2026-04-20T15:00:00Z",
    "end": "2026-04-20T15:30:00Z"
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
      "agenda": "string",
      "allowAnyUserToBeCoHost": true,
      "dialInIpAddress": "string",
      "enabledAutoRecordMeeting": true,
      "enabledJoinBeforeHost": true,
      "end": "2026-05-07T12:00:00.000Z",
      "excludePassword": true,
      "hostDisplayName": "Ava Chen",
      "hostEmail": "ava@example.com",
      "hostUserId": "string",
      "id": "string",
      "joinBeforeHostMinutes": 1,
      "meetingNumber": "string",
      "meetingType": "string",
      "password": "string",
      "phoneAndVideoSystemPassword": "string",
      "publicMeeting": true,
      "recurrence": "string",
      "reminderTime": 1,
      "scheduledType": "string",
      "sessionTypeId": 1,
      "sipAddress": "string",
      "siteUrl": "https://example.com",
      "start": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "timezone": "string",
      "title": "string",
      "unlockedMeetingJoinSecurity": "string",
      "webLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Meeting action reference](actions/create-meeting.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webex/latest/actions/create-meeting).
