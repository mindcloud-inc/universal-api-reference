# ServiceM8: List Staff Members



```
GET https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-staff-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-staff-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-staff-members?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | Example: `active eq 1`. |

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
      "editDate": "string",
      "email": "ava@example.com",
      "first": "string",
      "geoTimestamp": "string",
      "hideFromSchedule": 1,
      "jobTitle": "string",
      "labourMaterialUuid": "string",
      "last": "string",
      "lat": 1,
      "lng": 1,
      "mobile": "string",
      "navigatingExpiryTimestamp": "string",
      "navigatingTimestamp": "string",
      "navigatingToJobUuid": "string",
      "securityRoleUuid": "string",
      "statusMessage": "string",
      "statusMessageTimestamp": "string",
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
| `editDate` | string |  |
| `email` | string |  |
| `first` | string |  |
| `geoTimestamp` | string |  |
| `hideFromSchedule` | number |  |
| `jobTitle` | string |  |
| `labourMaterialUuid` | string |  |
| `last` | string |  |
| `lat` | number |  |
| `lng` | number |  |
| `mobile` | string |  |
| `navigatingExpiryTimestamp` | string |  |
| `navigatingTimestamp` | string |  |
| `navigatingToJobUuid` | string |  |
| `securityRoleUuid` | string |  |
| `statusMessage` | string |  |
| `statusMessageTimestamp` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native ServiceM8 API, this operation is `GET /api_1.0/staff.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-staff-members.md) for the provider-specific parameters and requirements.

