# Start Or Stop Timer with MILKEE

Starts or stops a timer in MILKEE.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:companyId/times/timer`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Start Or Stop Timer](https://apidocs.milkee.ch/api/resources/times.html#start-stop-timer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billable` | body | `boolean` | no | Whether the running timer is billable. |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `description` | body | `string` | no | Work description when stopping a timer. |
| `end` | body | `string` | no | Optional stop time in H:i format when stopping a timer. |
| `project_id` | body | `number` | no | Project ID when starting a timer. |
