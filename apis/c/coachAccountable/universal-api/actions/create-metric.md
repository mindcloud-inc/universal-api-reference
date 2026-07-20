# CoachAccountable: Create Metric

Creates a metric in CoachAccountable.

```
POST https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-metric
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-metric" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1,
  "name": "Ava Chen",
  "units": "string",
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-metric', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": 1,
    "name": "Ava Chen",
    "units": "string",
    "startDate": "2026-05-07T12:00:00.000Z",
    "endDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | yes | The ID of the Client who will be tracking this Metric. |
| `name` | string | yes |  |
| `units` | string | yes | The unit of measure for numbers to be reported, like "$", "lbs", or "minutes". |
| `startDate` | date | yes | The date at which tracking is to be done. |
| `endDate` | date | yes | The date through which tracking is to be done. |
| `doTarget` | boolean | no | Should a target apply for this Metric? Default: `false`. |
| `targetStart` | number | no | If a target, what should be the starting value? |
| `targetEnd` | number | no | If a target, what should be the endgin value? |
| `targetMode` | list | no | Dictates how the graph is to be colored regarding being over/under the target values, if set. One of: `H`, `L`. Default: `H`. |
| `dataMode` | list | no | Cumulative means that numbers as reported are to be added to a running total. One of: `C`, `R`. Default: `R`. |
| `repeatRule` | list | no | On what frequency should values be reported for this Metric? One of: `MWF`, `TR`, `bidaily`, `bimonthlyDOM`, `bimonthlyDOW`, `biweekly`, `customWeekly`, `daily`, `monthlyDOM`, `monthlyDOW`, `monthlyLastDOM`, `none`, `quarterlyDOM`, `weekdays`, `weekly`. Default: `weekdays`. |
| `setReminders` | boolean | no | Shall a regular reminder be set for this Metric? Default: `false`. |
| `reminderMode` | list | no | On which basis should reminders be sent? One of: `DO`, `DS`. |
| `remindSendMethod` | list | no | How shall the recurring reminders be sent to your client for this Metric? One of: `E`, `T`. Default: `E`. |
| `remindTime` | string | no | Time of day at which the reminder should be sent on called-for days. |
| `remindDays` | number | no | Number of days since the last reporting that a reminder should be sent (applies only to the "DS" option for reminderMode). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "MetricID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `MetricID` | number |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-metric.md) for the provider-specific parameters and requirements.

