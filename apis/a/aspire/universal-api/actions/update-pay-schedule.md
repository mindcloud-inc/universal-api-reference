# Aspire: Update Pay Schedule

Updates an existing pay schedule in your Aspire account.

```
PUT https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-pay-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-pay-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payScheduleName": "Ava Chen",
  "dailyHoursBeforeOt": 1,
  "weeklyHoursBeforeOt": 1,
  "active": true,
  "defaultOtPayCodeId": 1,
  "defaultPayCodeId": 1,
  "payScheduleId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-pay-schedule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payScheduleName": "Ava Chen",
    "dailyHoursBeforeOt": 1,
    "weeklyHoursBeforeOt": 1,
    "active": true,
    "defaultOtPayCodeId": 1,
    "defaultPayCodeId": 1,
    "payScheduleId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payScheduleName` | string | yes |  |
| `dailyHoursBeforeOt` | number | yes |  |
| `weeklyHoursBeforeOt` | number | yes |  |
| `active` | boolean | yes |  |
| `defaultOtPayCodeId` | number | yes |  |
| `defaultPayCodeId` | number | yes |  |
| `payScheduleId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "PayScheduleID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `PayScheduleID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `PUT PaySchedules` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pay-schedule.md) for the provider-specific parameters and requirements.

