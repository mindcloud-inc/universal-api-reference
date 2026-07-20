# Get Time Entry by External ID with Timelink

Finds a time entry in Timelink by external ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/timeEntries/ext/:extId`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Get Time Entry by External ID](https://api.timelink.io/documentation#/Time%20Entries/get_api_v1_timeEntries_ext__ext-id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extId` | path | `string` | yes | The external reference ID for the time entry. |
