# Zoho Webinar Universal API Examples

These examples use the MindCloud API key and Zoho Webinar connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organization Details

Retrieves organization and user details from Zoho Webinar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/get-organization-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/get-organization-details?${params}`, {
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
      "featureAvailability": {},
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

See the full [Get Organization Details action reference](actions/get-organization-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoWebinar/latest/actions/get-organization-details).

## Bulk Register Webinar

Creates webinar registrations in Zoho Webinar in bulk.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/bulk-register-webinar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "{{credentials.organizationId}}",
  "webinarKey": "string",
  "registrant": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/bulk-register-webinar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "{{credentials.organizationId}}",
    "webinarKey": "string",
    "registrant": {}
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
      "failedCount": 1,
      "registeredCount": 1,
      "registrant": [
        {}
      ],
      "sessionDetails": {},
      "successCount": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Bulk Register Webinar action reference](actions/bulk-register-webinar.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoWebinar/latest/actions/bulk-register-webinar).
