# Zoho Meeting: Create Webinar Registrations

Creates webinar registrations in bulk in Zoho Meeting.

```
POST https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/create-webinar-registrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Meeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/create-webinar-registrations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "{{credentials.organizationId}}",
  "webinarKey": "string",
  "registrant[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/create-webinar-registrations', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "{{credentials.organizationId}}",
    "webinarKey": "string",
    "registrant[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | Organization ID (zsoid) from Get Current User Details. Default: `{{credentials.organizationId}}`. |
| `webinarKey` | string | yes | Webinar key returned by List Webinars or Create Webinar. |
| `sendMail` | boolean | no | Whether to send webinar registration emails. |
| `instanceId` | string | no | Event instance ID when required by Zoho. |
| `registrant[]` | array<object> | yes | Array of registrant objects with email, firstName, and lastName. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failedCount": 1,
      "registeredCount": 1,
      "registrant": [
        {
          "email": "ava@example.com",
          "joinLink": "https://example.com"
        }
      ],
      "sessionDetails": {
        "pendingCount": 1,
        "totalSessionCount": 1
      },
      "successCount": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failedCount` | number |  |
| `registeredCount` | number |  |
| `registrant[].email` | string |  |
| `registrant[].joinLink` | string |  |
| `sessionDetails.pendingCount` | number |  |
| `sessionDetails.totalSessionCount` | number |  |
| `successCount` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Zoho Meeting API, this operation is `POST /api/v2/:organizationId/register/:webinarKey.json` (base URL `https://meeting.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webinar-registrations.md) for the provider-specific parameters and requirements.

