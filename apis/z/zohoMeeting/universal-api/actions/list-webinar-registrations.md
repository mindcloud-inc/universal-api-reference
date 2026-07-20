# Zoho Meeting: List Webinar Registrations

Retrieves webinar registrations from Zoho Meeting.

```
GET https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/list-webinar-registrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Meeting `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/list-webinar-registrations?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=%7B%7Bcredentials.organizationId%7D%7D&webinarKey=string&status=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "{{credentials.organizationId}}",
  "webinarKey": "string",
  "status": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/list-webinar-registrations?${params}`, {
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
| `webinarKey` | string | yes | Webinar key returned by Create Webinar or List Webinars. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | yes | Registration approval status filter: 1 auto approval, 0 manual approval, 2 denied by organiser, 3 cancelled by registrant. |
| `sysId` | string | no | Optional event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "approvedCount": 1,
        "deniedCount": 1,
        "isAutoApprovalEnabled": true,
        "pendingCount": 1,
        "totalCount": 1
      },
      "registrants": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.approvedCount` | number |  |
| `meta.deniedCount` | number |  |
| `meta.isAutoApprovalEnabled` | boolean |  |
| `meta.pendingCount` | number |  |
| `meta.totalCount` | number |  |
| `registrants[]` | array<object> |  |
| `registrants[].approvalStatus` | string |  |
| `registrants[].countryName` | string |  |
| `registrants[].email` | string |  |
| `registrants[].joinLink` | string |  |
| `registrants[].regionName` | string |  |
| `registrants[].registeredTime` | string |  |
| `registrants[].registeredTimeInMilliSec` | number |  |
| `registrants[].registeredTimezone` | string |  |
| `registrants[].registerId` | string |  |
| `registrants[].registerKey` | string |  |
| `registrants[].status` | string |  |
| `registrants[].userName` | string |  |

## Native endpoint

Through the native Zoho Meeting API, this operation is `GET /api/v2/:organizationId/registration/:webinarKey` (base URL `https://meeting.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webinar-registrations.md) for the provider-specific parameters and requirements.

