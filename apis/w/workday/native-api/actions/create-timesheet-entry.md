# Create Timesheet Entry with Workday

Create a worker time block in Workday Time Tracking for a specific worker using either quantity-based or clock-in and clock-out entry fields.

## Endpoint

- **Method:** `POST`
- **Path:** `workers/:ID/workerTimeBlock`
- **Base URL:** `{restAPIBaseURL}/`
- **Official documentation:** [Create Timesheet Entry](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/post-/workers/-ID-/workerTimeBlock)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ID` | path | `string` | yes | The Workday ID of the worker for whom the time block will be created. |
| `calendarDate` | body | `date` | no | Required for hourly entry together with Reported Quantity. |
| `reportedQuantity` | body | `number` | no | Required for hourly entry together with Calendar Date. |
| `inTime` | body | `date` | no | Required for in/out entry together with Out Time, In Time Zone ID, and Out Time Zone ID. |
| `outTime` | body | `date` | no | Required for in/out entry together with In Time, In Time Zone ID, and Out Time Zone ID. |
| `inTimeZone` | body | `object` | no | Reference object for the in time zone. |
| `inTimeZone.id` | body | `string` | no | The Workday ID for the selected in time zone reference. |
| `outTimeZone` | body | `object` | no | Reference object for the out time zone. |
| `outTimeZone.id` | body | `string` | no | The Workday ID for the selected out time zone reference. |
| `timeEntryCode` | body | `object` | no | Reference object for the selected time entry code. |
| `timeEntryCode.id` | body | `string` | no | The Workday ID for the selected time entry code reference. |
| `project` | body | `object` | no | Reference object for the selected project. |
| `project.id` | body | `string` | no | The Workday ID for the selected project reference. |
| `projectPlanTask` | body | `object` | no | Reference object for the selected project plan task. |
| `projectPlanTask.id` | body | `string` | no | The Workday ID for the selected project plan task reference. |
