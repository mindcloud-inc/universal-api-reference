# ServiceM8: Update Staff Member



```
PUT https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/update-staff-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/update-staff-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string",
  "first": "string",
  "last": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/update-staff-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string",
    "first": "string",
    "last": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | UUID of the Staff Member |
| `first` | string | yes | Staff First Name |
| `last` | string | yes | Staff Last Name |
| `email` | string | yes | Staff Email Address. This is also your login name. |
| `mobile` | string | no | Mobile phone number of the staff member. Used for SMS communications and identification when calling. |
| `jobTitle` | string | no | The staff member's job title or role within the organization. |
| `color` | string | no | The color assigned to this staff member, represented as a hex color code. |
| `hideFromSchedule` | number | no | Boolean flag controlling whether this staff member appears in the schedule view. |
| `lng` | number | no | Longitude coordinate of the staff member's current or last known location. Used for tracking staff locations and calculating routes and travel distances. |
| `lat` | number | no | Latitude coordinate of the staff member's current or last known location. Used for tracking staff locations and calculating routes and travel distances. |
| `geoTimestamp` | date | no | The date and time when the staff member's geographic location was last updated. |
| `navigatingToJobUuid` | string | no | UUID of the job the staff member is currently navigating to. |
| `navigatingTimestamp` | date | no | The date and time when the staff member started navigating to a job. |
| `navigatingExpiryTimestamp` | date | no | The date and time when navigation to a job is expected to complete or expire. |
| `statusMessage` | string | no | Short message summarising the staff's current status. |
| `statusMessageTimestamp` | date | no | The date and time when the staff member's status message was last updated. |
| `canReceivePushNotification` | string | no | Whether the staff member can receive push notifications. |
| `securityRoleUuid` | string | no | Security role UUID. |
| `labourMaterialUuid` | string | no | Labour material UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recordUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recordUuid` | string | UUID of the updated staff member. |

## Native endpoint

Through the native ServiceM8 API, this operation is `POST /api_1.0/staff/:uuid.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-staff-member.md) for the provider-specific parameters and requirements.

