# Create Logged Time Entry with Streamtime

## Endpoint

- **Method:** `POST`
- **Path:** `/logged_times`
- **Base URL:** `https://api.streamtime.net/v2`
- **Official documentation:** [Create Logged Time Entry](https://api.streamtime.net/v2/swagger#/ToDos/createLoggedTime)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `number` | yes | User ID for the logged time entry. |
| `date` | body | `string` | yes | Date for the logged time entry. |
| `minutes` | body | `number` | yes | Tracked minutes for the logged time entry. |
| `jobId` | body | `number` | no | Job ID linked to the logged time entry. |
| `jobItemUserId` | body | `number` | no | Job item user ID linked to the logged time entry. |
| `notes` | body | `string` | no | Notes for the logged time entry. |
| `private` | body | `boolean` | no | Whether the logged time entry is private. |
| `loggedTimeStatus` | body | `object` | no | Logged time status object. |
| `loggedTimeStatus.id` | body | `list<number>` | yes | Logged Time Status ID (1=Incomplete, 2=Complete, 3=Deleted). Accepted values: `1`, `2`, `3`. |
