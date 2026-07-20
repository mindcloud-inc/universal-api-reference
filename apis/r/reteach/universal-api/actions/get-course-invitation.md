# Reteach: Get Course Invitation



```
GET https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-course-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reteach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-course-invitation?connectionId=$CONNECTION_ID&courseInvitationId=d5e03c9d-0a6b-4dd1-bdb0-949093158019" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseInvitationId": "d5e03c9d-0a6b-4dd1-bdb0-949093158019"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-course-invitation?${params}`, {
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
| `courseInvitationId` | string | yes | The id of the course invitation. Default: `d5e03c9d-0a6b-4dd1-bdb0-949093158019`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessTime": 1,
      "accessTimeUnit": "string",
      "certificateExpiresAfter": 1,
      "certificateExpiresAfterUnit": "string",
      "course": {},
      "customer": {},
      "customerGroup": {},
      "deadline": "string",
      "id": "string",
      "isCertificateEnabled": true,
      "isMandatory": true,
      "isNotificationEnabled": true,
      "isRelative": true,
      "isRepeating": true,
      "repeatingInterval": 1,
      "repeatingIntervalUnit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessTime` | number |  |
| `accessTimeUnit` | string |  |
| `certificateExpiresAfter` | number |  |
| `certificateExpiresAfterUnit` | string |  |
| `course` | object |  |
| `customer` | object |  |
| `customerGroup` | object |  |
| `deadline` | string |  |
| `id` | string |  |
| `isCertificateEnabled` | boolean |  |
| `isMandatory` | boolean |  |
| `isNotificationEnabled` | boolean |  |
| `isRelative` | boolean |  |
| `isRepeating` | boolean |  |
| `repeatingInterval` | number |  |
| `repeatingIntervalUnit` | string |  |

## Native endpoint

Through the native Reteach API, this operation is `GET /v1/course-invitation/{courseInvitationId}` (base URL `https://api.reteach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-course-invitation.md) for the provider-specific parameters and requirements.

