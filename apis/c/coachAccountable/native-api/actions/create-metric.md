# Create Metric with CoachAccountable

Creates a metric in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Create Metric](https://www.coachaccountable.com/APIDocs#Metric.add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | The ID of the Client who will be tracking this Metric. |
| `name` | body | `string` | yes | — |
| `units` | body | `string` | yes | The unit of measure for numbers to be reported, like "$", "lbs", or "minutes". |
| `startDate` | body | `date` | yes | The date at which tracking is to be done. |
| `endDate` | body | `date` | yes | The date through which tracking is to be done. |
| `doTarget` | body | `boolean` | no | Should a target apply for this Metric? |
| `targetStart` | body | `number` | no | If a target, what should be the starting value? |
| `targetEnd` | body | `number` | no | If a target, what should be the endgin value? |
| `targetMode` | body | `list` | no | Dictates how the graph is to be colored regarding being over/under the target values, if set. Accepted values: `H`, `L`. |
| `dataMode` | body | `list` | no | Cumulative means that numbers as reported are to be added to a running total. Accepted values: `C`, `R`. |
| `repeatRule` | body | `list` | no | On what frequency should values be reported for this Metric? Accepted values: `MWF`, `TR`, `bidaily`, `bimonthlyDOM`, `bimonthlyDOW`, `biweekly`, `customWeekly`, `daily`, `monthlyDOM`, `monthlyDOW`, `monthlyLastDOM`, `none`, `quarterlyDOM`, `weekdays`, `weekly`. |
| `setReminders` | body | `boolean` | no | Shall a regular reminder be set for this Metric? |
| `reminderMode` | body | `list` | no | On which basis should reminders be sent? Accepted values: `DO`, `DS`. |
| `remindSendMethod` | body | `list` | no | How shall the recurring reminders be sent to your client for this Metric? Accepted values: `E`, `T`. |
| `remindTime` | body | `string` | no | Time of day at which the reminder should be sent on called-for days. |
| `remindDays` | body | `number` | no | Number of days since the last reporting that a reminder should be sent (applies only to the "DS" option for reminderMode). |
