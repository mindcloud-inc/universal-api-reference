# Update Logged Time Entry with Streamtime

## Endpoint

- **Method:** `PUT`
- **Path:** `/logged_times/:logged_time_id`
- **Base URL:** `https://api.streamtime.net/v2`
- **Official documentation:** [Update Logged Time Entry](https://api.streamtime.net/v2/swagger#/ToDos/updateLoggedTime)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logged_time_id` | path | `number` | yes | Logged time entry ID. |
| `userId` | body | `number` | no | User ID for the logged time entry. |
| `date` | body | `string` | no | Date for the logged time entry. |
| `minutes` | body | `number` | no | Tracked minutes for the logged time entry. |
| `jobId` | body | `number` | no | Job ID linked to the logged time entry. |
| `jobItemUserId` | body | `number` | no | Job item user ID linked to the logged time entry. |
| `notes` | body | `string` | no | Notes for the logged time entry. |
| `private` | body | `boolean` | no | Whether the logged time entry is private. |
| `loggedTimeStatus` | body | `object` | no | Logged time status object. |
| `loggedTimeStatus.id` | body | `list<number>` | no | Logged Time Status ID (1=Incomplete, 2=Complete, 3=Deleted). Accepted values: `1`, `2`, `3`. |
