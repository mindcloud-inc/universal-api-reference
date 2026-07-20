# Zoho Webinar: Get Organization Details

Retrieves organization and user details from Zoho Webinar.

```
GET https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/get-organization-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Webinar `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `daysLeft` | number |  |
| `displayName` | string |  |
| `edition` | string |  |
| `featureAvailability` | object |  |
| `fullName` | string |  |
| `isAdmin` | boolean |  |
| `isCRMMeetingUser` | boolean |  |
| `isfreeUser` | boolean |  |
| `isMeetingFreeUser` | boolean |  |
| `isMeetingPaidUser` | boolean |  |
| `isMeetingTrialUser` | boolean |  |
| `isPaidUser` | boolean |  |
| `isPrivilegedUser` | boolean |  |
| `isRecordingAddonUser` | boolean |  |
| `isTollfreeUser` | boolean |  |
| `isTrialUser` | boolean |  |
| `isWebinarFreeUser` | boolean |  |
| `isWebinarPaidUser` | boolean |  |
| `isWebinarTrialUser` | boolean |  |
| `isZVPMeeting` | boolean |  |
| `meetingRedirectionServer` | string |  |
| `orgName` | string |  |
| `participantCount` | number |  |
| `portalName` | string |  |
| `primaryEmail` | string |  |
| `redirectionServer` | string |  |
| `superAdminZuid` | number |  |
| `userCount` | number |  |
| `zsoid` | number |  |
| `zuid` | number |  |

## Native endpoint

Through the native Zoho Webinar API, this operation is `GET /api/v2/user.json` (base URL `https://webinar.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-details.md) for the provider-specific parameters and requirements.

