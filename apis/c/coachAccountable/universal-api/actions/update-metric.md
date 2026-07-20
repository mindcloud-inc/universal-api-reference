# CoachAccountable: Update Metric

Updates a metric in CoachAccountable.

```
PUT https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/update-metric
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/update-metric" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "metricId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/update-metric', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "metricId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metricId` | number | yes | ID of the Metric to be updated. |
| `name` | string | no | New name for the Metric, if to be changed. |
| `units` | string | no | The unit of measure for numbers to be reported, like "$", "lbs", or "minutes". |
| `startDate` | date | no | The date at which tracking is to be done. |
| `endDate` | date | no | The date through which tracking is to be done. |
| `doTarget` | boolean | no | Should a target apply for this Metric? |
| `targetStart` | number | no | If a target, what should be the starting value? |
| `targetEnd` | number | no | If a target, what should be the endgin value? |
| `targetMode` | list | no | Dictates how the graph is to be colored regarding being over/under the target values, if set. One of: `H`, `L`. |
| `dataMode` | list | no | Cumulative means that numbers as reported are to be added to a running total. One of: `C`, `R`. |
| `repeatRule` | list | no | On what frequency should values be reported for this Metric? One of: `MWF`, `TR`, `bidaily`, `bimonthlyDOM`, `bimonthlyDOW`, `biweekly`, `customWeekly`, `daily`, `monthlyDOM`, `monthlyDOW`, `monthlyLastDOM`, `none`, `quarterlyDOM`, `weekdays`, `weekly`. |
| `setReminders` | boolean | no | Shall a regular reminder be set for this Metric? |
| `reminderMode` | list | no | On which basis should reminders be sent? One of: `DO`, `DS`. |
| `remindSendMethod` | list | no | Send true to notify the client via email of this new Action. One of: `E`, `T`. |
| `remindTime` | string | no | Time of day at which the reminder should be sent on called-for days. |
| `remindDays` | number | no | Number of days since the last reporting that a reminder should be sent (applies only to the "DS" option for reminderMode). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CoachAccountable API returns.

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-metric.md) for the provider-specific parameters and requirements.

