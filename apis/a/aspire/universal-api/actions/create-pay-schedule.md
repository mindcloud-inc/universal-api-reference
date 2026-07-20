# Aspire: Create Pay Schedule



```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-pay-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-pay-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "active": true,
  "dailyHoursBeforeOt": 1,
  "weeklyHoursBeforeOt": 1,
  "payScheduleName": "Ava Chen",
  "defaultOtPayCodeId": 1,
  "defaultPayCodeId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-pay-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "active": true,
    "dailyHoursBeforeOt": 1,
    "weeklyHoursBeforeOt": 1,
    "payScheduleName": "Ava Chen",
    "defaultOtPayCodeId": 1,
    "defaultPayCodeId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | boolean | yes |  |
| `dailyHoursBeforeOt` | number | yes |  |
| `weeklyHoursBeforeOt` | number | yes |  |
| `payScheduleName` | string | yes |  |
| `defaultOtPayCodeId` | list<number> | yes |  |
| `defaultPayCodeId` | list<number> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "payScheduleID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `payScheduleID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `POST PaySchedules` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pay-schedule.md) for the provider-specific parameters and requirements.

