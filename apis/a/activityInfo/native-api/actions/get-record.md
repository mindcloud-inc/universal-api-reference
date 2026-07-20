# Get Record with ActivityInfo

Retrieves a record from an ActivityInfo form.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/form/:formId/record/:recordId`
- **Base URL:** `https://www.activityinfo.org`
- **Official documentation:** [Get Record](https://www.activityinfo.org/support/docs/api/reference/getRecord.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ActivityInfo form ID. |
| `recordId` | path | `string` | yes | ActivityInfo record ID. |
