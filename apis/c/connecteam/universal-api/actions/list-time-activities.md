# Connecteam: List Time Activities

Retrieve a list of time activities in under a specified time clock.
Time activities include shift and/or manual breaks

```
GET https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-time-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-time-activities?connectionId=$CONNECTION_ID&timeClockId=1&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timeClockId": "1",
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-time-activities?${params}`, {
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
| `timeClockId` | number | yes |  |
| `startDate` | string | yes |  |
| `endDate` | string | yes |  |
| `userIds` | array<number> | no | Accepts multiple values as an array. |
| `jobIds` | array<string> | no | Accepts multiple values as an array. |
| `manualBreakIds` | array<string> | no | Accepts multiple values as an array. |
| `policyTypeIds` | array<string> | no | Accepts multiple values as an array. |
| `activityTypes` | array<string> | no | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `userId` | number |  |

## Native endpoint

Through the native Connecteam API, this operation is `GET /time-clock/v1/time-clocks/:timeClockId/time-activities` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-activities.md) for the provider-specific parameters and requirements.

