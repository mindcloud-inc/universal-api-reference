# Zoho Meeting: Get Current License Details

Retrieves current license details from Zoho Meeting.

```
GET https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-current-license-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Meeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-current-license-details?connectionId=$CONNECTION_ID&organizationId=%7B%7Bcredentials.organizationId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "{{credentials.organizationId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-current-license-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | Organization ID (zsoid) from Get Current User Details. Default: `{{credentials.organizationId}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addonEligibility": true,
      "isBundleUser": true,
      "licenseType": "string",
      "meetingAddon": {
        "edition": "string",
        "licenseType": "string",
        "noOfLicenseEnabled": "string",
        "noOfLicenseLeft": "string",
        "noOfUsers": "string",
        "participantCount": "string"
      },
      "recordingAddon": {
        "enabled": true
      },
      "resourceType": "string",
      "tollFreeAddon": {
        "countryCount": 1,
        "enabled": true
      },
      "trialExpiryTime": "string",
      "webinarAddon": {
        "attendeeCount": "string",
        "edition": "string",
        "licenseType": "string",
        "noOfLicenseEnabled": "string",
        "noOfLicenseLeft": "string",
        "noOfUsers": "string"
      },
      "webinarTrialExpiryTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addonEligibility` | boolean |  |
| `isBundleUser` | boolean |  |
| `licenseType` | string |  |
| `meetingAddon.edition` | string |  |
| `meetingAddon.licenseType` | string |  |
| `meetingAddon.noOfLicenseEnabled` | string |  |
| `meetingAddon.noOfLicenseLeft` | string |  |
| `meetingAddon.noOfUsers` | string |  |
| `meetingAddon.participantCount` | string |  |
| `recordingAddon.enabled` | boolean |  |
| `resourceType` | string |  |
| `tollFreeAddon.countryCount` | number |  |
| `tollFreeAddon.enabled` | boolean |  |
| `trialExpiryTime` | string |  |
| `webinarAddon.attendeeCount` | string |  |
| `webinarAddon.edition` | string |  |
| `webinarAddon.licenseType` | string |  |
| `webinarAddon.noOfLicenseEnabled` | string |  |
| `webinarAddon.noOfLicenseLeft` | string |  |
| `webinarAddon.noOfUsers` | string |  |
| `webinarTrialExpiryTime` | string |  |

## Native endpoint

Through the native Zoho Meeting API, this operation is `GET /api/v2/:organizationId/license` (base URL `https://meeting.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-license-details.md) for the provider-specific parameters and requirements.

