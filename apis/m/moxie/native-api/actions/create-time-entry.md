# Create Time Entry with Moxie

Creates a new time entry in Moxie.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/timeWorked/create`
- **Base URL:** `https://pod01.withmoxie.com/api/public`
- **Official documentation:** [Create Time Entry](https://help.withmoxie.com/en/articles/8160498-create-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timerStart` | body | `date` | yes | Time entry start timestamp. |
| `timerEnd` | body | `date` | yes | Time entry end timestamp. |
| `userEmail` | body | `string` | yes | Email of the user logging time. |
| `clientName` | body | `string` | no | Client name for the time entry. |
| `projectName` | body | `string` | no | Project name for the time entry. |
| `deliverableName` | body | `string` | no | Deliverable name for the time entry. |
| `notes` | body | `string` | no | Notes for the time entry. |
| `createClient` | body | `boolean` | no | Create the client if it does not exist. |
| `createProject` | body | `boolean` | no | Create the project if it does not exist. |
| `createDeliverable` | body | `boolean` | no | Create the deliverable if it does not exist. |
