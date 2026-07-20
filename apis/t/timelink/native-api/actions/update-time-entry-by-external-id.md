# Update Time Entry by External ID with Timelink

Updates an existing time entry in Timelink by external ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/timeEntries/ext/:extId`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Update Time Entry by External ID](https://api.timelink.io/documentation#/Time%20Entries/patch_api_v1_timeEntries_ext_ext-id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extId` | path | `string` | yes | The external reference ID for the time entry. |
| `description` | body | `string` | no | Updated time entry description. |
| `ended_at` | body | `string` | no | Updated end timestamp. |
