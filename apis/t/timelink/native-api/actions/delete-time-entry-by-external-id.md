# Delete Time Entry by External ID with Timelink

Deletes an existing time entry from Timelink by external ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/timeEntries/ext/:extId`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Delete Time Entry by External ID](https://api.timelink.io/documentation#/Time%20Entries/delete_api_v1_timeEntries_ext__ext-id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extId` | path | `string` | yes | The external reference ID for the time entry. |
