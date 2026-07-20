# Zoho Meeting: Get User Details

Retrieves user details from Zoho Meeting.

```
GET https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-user-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Meeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-user-details?connectionId=$CONNECTION_ID&organizationId=%7B%7Bcredentials.organizationId%7D%7D&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "{{credentials.organizationId}}",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-user-details?${params}`, {
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
| `userId` | string | yes | User ID returned by List Users. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailId": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "lastName": "Chen",
      "meetingLicense": {
        "edition": "string",
        "enabled": true
      },
      "organization": {
        "isDefault": true,
        "link": "https://example.com",
        "orgId": "string",
        "orgName": "Ava Chen"
      },
      "resourceType": "string",
      "role": "string",
      "userId": "string",
      "webinarLicense": {
        "edition": "string",
        "enabled": true
      },
      "zuid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailId` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `lastName` | string |  |
| `meetingLicense.edition` | string |  |
| `meetingLicense.enabled` | boolean |  |
| `organization.isDefault` | boolean |  |
| `organization.link` | string |  |
| `organization.orgId` | string |  |
| `organization.orgName` | string |  |
| `resourceType` | string |  |
| `role` | string |  |
| `userId` | string |  |
| `webinarLicense.edition` | string |  |
| `webinarLicense.enabled` | boolean |  |
| `zuid` | number |  |

## Native endpoint

Through the native Zoho Meeting API, this operation is `GET /api/v2/:organizationId/user/:userId` (base URL `https://meeting.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-details.md) for the provider-specific parameters and requirements.

