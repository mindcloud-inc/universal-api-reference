# List Time Entries with UKG Ready

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/companies/:cid/time-entries`
- **Base URL:** `https://{hostname}/ta/rest`
- **Official documentation:** [List Time Entries](https://secure7.saashr.com/ta/docs/rest/public)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | no | minimum date of time entry. Example: 2016-05-01 |
| `end_date` | query | `string` | no | maximum date of time entry. Example: 2016-05-30 |
| `cid` | path | `string` | no | — |
| `is_light` | query | `boolean` | no | Use light request containing only raw time entry data, no calculated time. |
