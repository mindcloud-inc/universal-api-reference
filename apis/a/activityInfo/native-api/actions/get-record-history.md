# Get Record History with ActivityInfo

Retrieves a record's history from ActivityInfo.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/form/:formId/record/:recordId/history`
- **Base URL:** `https://www.activityinfo.org`
- **Official documentation:** [Get Record History](https://www.activityinfo.org/support/docs/api/reference/getRecordHistory.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ActivityInfo form ID. |
| `recordId` | path | `string` | yes | ActivityInfo record ID. |
