# Connecteam: Create Time Off Request

Create a new time-off request for a user under a specified policy. The time-off request can be either in pending or approved status.

```
POST https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/create-time-off-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/create-time-off-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": 1,
  "policyTypeId": "string",
  "isAllDay": true,
  "startDate": "string",
  "endDate": "string",
  "timezone": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/create-time-off-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": 1,
    "policyTypeId": "string",
    "isAllDay": true,
    "startDate": "string",
    "endDate": "string",
    "timezone": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeClockId` | number | no |  |
| `userId` | number | yes |  |
| `policyTypeId` | string | yes |  |
| `isAllDay` | boolean | yes |  |
| `startDate` | string | yes |  |
| `endDate` | string | yes |  |
| `startTime` | string | no |  |
| `endTime` | string | no |  |
| `timezone` | string | yes |  |
| `status` | string | yes |  |
| `employeeNote` | string | no |  |
| `managerNote` | string | no |  |
| `isAdjustForDayLightSaving` | boolean | no | Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "employeeNote": "string",
      "endDate": "string",
      "endTime": "string",
      "id": "string",
      "isAllDay": true,
      "managerNote": "string",
      "policyTypeId": "string",
      "startDate": "string",
      "startTime": "string",
      "status": "string",
      "timeClockId": 1,
      "timezone": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `employeeNote` | string |  |
| `endDate` | string |  |
| `endTime` | string |  |
| `id` | string |  |
| `isAllDay` | boolean |  |
| `managerNote` | string |  |
| `policyTypeId` | string |  |
| `startDate` | string |  |
| `startTime` | string |  |
| `status` | string |  |
| `timeClockId` | number |  |
| `timezone` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Connecteam API, this operation is `POST /time-off/v1/requests` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-off-request.md) for the provider-specific parameters and requirements.

