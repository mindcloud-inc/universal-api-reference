# Delete Many Records with NileDesk

Deletes multiple matched records from NileDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/DeleteManyRecords`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Delete Many Records](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | yes | The NileDesk filter object used to select the records to delete. |
| `template_id` | body | `string` | yes | The NileDesk template containing the records to delete. |
