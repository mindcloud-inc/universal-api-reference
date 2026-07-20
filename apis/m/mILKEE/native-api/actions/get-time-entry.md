# Get Time Entry with MILKEE

Retrieves a time entry from MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/times/:timeId`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Get Time Entry](https://apidocs.milkee.ch/api/resources/times.html#retrieve-a-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `time_id` | path | `string` | yes | The numeric MILKEE time entry ID used in the request path. |
