# Zoho Meeting Universal API Examples

These examples use the MindCloud API key and Zoho Meeting connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User Details

Retrieves current user details from Zoho Meeting.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-current-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-current-user-details?${params}`, {
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
      "daysLeft": 1,
      "displayName": "Ava Chen",
      "edition": "string",
      "fullName": "Ava Chen",
      "isAdmin": true,
      "isCRMMeetingUser": true,
      "isfreeUser": true,
      "isMeetingFreeUser": true,
      "isMeetingPaidUser": true,
      "isMeetingTrialUser": true,
      "isPaidUser": true,
      "isPrivilegedUser": true,
      "isRecordingAddonUser": true,
      "isTollfreeUser": true,
      "isTrialUser": true,
      "isWebinarFreeUser": true,
      "isWebinarPaidUser": true,
      "isWebinarTrialUser": true,
      "isZVPMeeting": true,
      "meetingRedirectionServer": "string",
      "orgName": "Ava Chen",
      "participantCount": 1,
      "portalName": "Ava Chen",
      "primaryEmail": "ava@example.com",
      "redirectionServer": "string",
      "superAdminZuid": 1,
      "userCount": 1,
      "zsoid": 1,
      "zuid": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Current User Details action reference](actions/get-current-user-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoMeeting/latest/actions/get-current-user-details).

## Create Meeting

Creates a new meeting in Zoho Meeting.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/create-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "{{credentials.organizationId}}",
  "topic": "string",
  "startTime": "string",
  "presenter": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/create-meeting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "{{credentials.organizationId}}",
    "topic": "string",
    "startTime": "string",
    "presenter": "string"
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
      "session": {
        "accessCode": "string",
        "creator": "string",
        "departmentId": "string",
        "departmentName": "Ava Chen",
        "dialinUrl": "https://example.com",
        "duration": 1,
        "endTime": "string",
        "isRecurring": true,
        "joinLink": "https://example.com",
        "meeting": {
          "zsoid": "string"
        },
        "meetingKey": "string",
        "presenter": 1,
        "presenterEmail": "ava@example.com",
        "registrationLink": "https://example.com",
        "startLink": "https://example.com",
        "startTime": "string",
        "sys_id": "string",
        "timezone": "string",
        "topic": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Meeting action reference](actions/create-meeting.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoMeeting/latest/actions/create-meeting).
