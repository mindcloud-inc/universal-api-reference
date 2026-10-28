# Update Time Entries with UKG Ready

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/companies/:cid/time-entries/collection`
- **Base URL:** `https://{hostname}/ta/rest`
- **Official documentation:** [Update Time Entries](https://secure7.saashr.com/ta/docs/rest/public)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | path | `string` | no | — |
| `time_entry_sets[].employee` | body | `object` | no | — |
| `time_entry_sets[].employee.account_id` | body | `number` | no | — |
| `time_entry_sets[].time_entries[].cost_centers[].index` | body | `number` | no | — |
| `time_entry_sets[].time_entries[].cost_centers[].value.id` | body | `number` | no | — |
| `time_entry_sets[].time_entries[].pay_category.id` | body | `number` | no | — |
| `time_entry_sets[].time_entries[].premium_shift.id` | body | `number` | no | — |
| `time_entry_sets[].time_entries[].time_off.id` | body | `number` | no | — |
| `time_entry_sets[]` | body | `array<object>` | no | — |
| `time_entry_sets[].time_entries[].cost_centers[]` | body | `array<object>` | no | — |
| `time_entry_sets[].time_entries[].cost_centers[].value` | body | `object` | no | — |
| `time_entry_sets[].time_entries[].type` | body | `list<string>` | no | — |
| `partial_update` | query | `boolean` | no | Use to update entries within the specified time range, instead of replacing them. |
| `time_entry_sets[].end_date` | body | `date` | no | Date needs to be in the format yyyy-mm-dd within the 1900-12-31 and 2079-06-05 date range |
| `time_entry_sets[].start_date` | body | `date` | no | Date needs to be in the format yyyy-mm-dd within the 1900-12-31 and 2079-06-05 date range |
| `time_entry_sets[].time_entries[].date` | body | `date` | no | Date needs to be in the format yyyy-mm-dd within the 1900-12-31 and 2079-06-05 date range |
| `time_entry_sets[].time_entries[].start_time` | body | `date` | no | (date-time) |
| `time_entry_sets[].time_entries[]` | body | `array<object>` | no | — |
| `time_entry_sets[].time_entries[].end_time` | body | `date` | no | (date-time) |
| `time_entry_sets[].time_entries[].total` | body | `number` | no | — |
| `time_entry_sets[].time_entries[].time_off` | body | `object` | no | — |
| `time_entry_sets[].time_entries[].pay_category` | body | `object` | no | — |
| `time_entry_sets[].time_entries[].premium_shift` | body | `object` | no | — |
| `time_entry_sets[].time_entries[].piecework` | body | `number` | no | — |
| `time_entry_sets[].time_entries[].amount` | body | `number` | no | — |
| `time_entry_sets[].time_entries[].from` | body | `date` | no | Date needs to be in the format yyyy-mm-dd within the 1900-12-31 and 2079-06-05 date range |
| `time_entry_sets[].time_entries[].to` | body | `date` | no | Date needs to be in the format yyyy-mm-dd within the 1900-12-31 and 2079-06-05 date range |
