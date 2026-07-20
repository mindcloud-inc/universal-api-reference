# Update Many Records with NileDesk

Updates multiple matched records in NileDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/UpdateManyRecords`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Update Many Records](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | body | `object` | yes | The field values to apply to the matching records. |
| `filters` | body | `object` | yes | The NileDesk filter object used to select the records to update. |
| `template_id` | body | `string` | yes | The NileDesk template containing the records to update. |
