# Add Attendance Entries with Zoho People

Creates attendance entries in Zoho People.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/attendance/entries`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Add Attendance Entries](https://www.zoho.com/people/api/v3/attendance/entries-bulk-add.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `punch_details` | body | `string` | yes | JSON array of attendance entries to add. |
| `datetime_format` | body | `string` | yes | Datetime format for the punch_details payload, for example yyyy-MM-dd HH:mm:ss. |
| `entries_timezone` | body | `string` | no | Timezone of the source entries, such as a biometric device timezone. |
| `storage_timezone` | body | `string` | no | Timezone to store the attendance entries in Zoho People. |
