# Count Records with NileDesk

Counts matching records in NileDesk by filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/CountRecords`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Count Records](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | Optional NileDesk filter object, for example {"logic":"and","rules":[{"field1":"value","operator":"eq"}]}. |
| `process_id` | body | `string` | no | Optional process or board item identifier to narrow the count. |
| `template_id` | body | `string` | yes | The NileDesk template to count records from. |
