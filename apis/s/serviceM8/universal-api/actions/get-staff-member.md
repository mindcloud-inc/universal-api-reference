# ServiceM8: Get Staff Member



```
GET https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/get-staff-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/get-staff-member?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/get-staff-member?${params}`, {
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
| `uuid` | string | yes | UUID of the Staff Member |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "canReceivePushNotification": 1,
      "color": "string",
      "customIconUrl": "https://example.com",
      "editDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "first": "string",
      "geoTimestamp": "2026-05-07T12:00:00.000Z",
      "hideFromSchedule": 1,
      "jobTitle": "string",
      "labourMaterialUuid": "string",
      "last": "string",
      "lat": 1,
      "lng": 1,
      "mobile": "string",
      "navigatingExpiryTimestamp": "2026-05-07T12:00:00.000Z",
      "navigatingTimestamp": "2026-05-07T12:00:00.000Z",
      "navigatingToJobUuid": "string",
      "securityRoleUuid": "string",
      "statusMessage": "string",
      "statusMessageTimestamp": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `canReceivePushNotification` | number |  |
| `color` | string |  |
| `customIconUrl` | string |  |
| `editDate` | date |  |
| `email` | string |  |
| `first` | string |  |
| `geoTimestamp` | date |  |
| `hideFromSchedule` | number |  |
| `jobTitle` | string |  |
| `labourMaterialUuid` | string |  |
| `last` | string |  |
| `lat` | number |  |
| `lng` | number |  |
| `mobile` | string |  |
| `navigatingExpiryTimestamp` | date |  |
| `navigatingTimestamp` | date |  |
| `navigatingToJobUuid` | string |  |
| `securityRoleUuid` | string |  |
| `statusMessage` | string |  |
| `statusMessageTimestamp` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native ServiceM8 API, this operation is `GET /api_1.0/staff/:uuid.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-staff-member.md) for the provider-specific parameters and requirements.

