# Zoho Meeting: List Users

Retrieves users from Zoho Meeting.

```
GET https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Meeting `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=%7B%7Bcredentials.organizationId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "{{credentials.organizationId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/list-users?${params}`, {
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
| `role` | string |  |
| `userId` | string |  |
| `webinarLicense.edition` | string |  |
| `webinarLicense.enabled` | boolean |  |
| `zuid` | number |  |

## Native endpoint

Through the native Zoho Meeting API, this operation is `GET /api/v2/:organizationId/user` (base URL `https://meeting.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

