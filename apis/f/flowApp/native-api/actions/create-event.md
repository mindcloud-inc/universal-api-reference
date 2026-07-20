# Create Event with Flow App

## Endpoint

- **Method:** `POST`
- **Path:** `/event`
- **Base URL:** `https://prod.flowapp.com/api/v1`
- **Official documentation:** [Create Event](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `published` | body | `boolean` | no | Whether to publish the event immediately or save it as a draft. |
| `creatorID` | body | `number` | yes | The numeric ID of the event creator. |
| `title` | body | `string` | yes | The event title. |
| `description` | body | `string` | yes | The event description shown on registration and access pages. |
| `date` | body | `string` | yes | The event date in YYYY-MM-DD format. |
| `time` | body | `string` | yes | The event time in 24-hour HH:MI:SS format. |
| `timezone` | body | `string` | yes | A MomentJS-compatible timezone string. |
| `operators[]` | body | `array<object>` | yes | Array of operator objects participating in the event. |
| `operators[].id` | body | `number` | yes | Operator ID in the operators array. |
| `operators[].role` | body | `number` | yes | Operator role where 5 is presenter and 10 is organizer. |
| `operators[].micEnabled` | body | `boolean` | yes | Whether the operator microphone is enabled. |
| `operators[].camEnabled` | body | `boolean` | yes | Whether the operator camera is enabled. |
| `operators[].screenSharingEnabled` | body | `boolean` | yes | Whether screen sharing is enabled for the operator. |
| `duration` | body | `number` | no | Estimated event duration in hours. |
| `earlyAccessPeriod` | body | `number` | no | Minutes before the event when attendees can begin logging in. |
| `videoRecord` | body | `boolean` | no | Whether the event should be recorded. |
| `onDemandReplays` | body | `boolean` | no | Whether attendees can register to view replays after the event ends. |
