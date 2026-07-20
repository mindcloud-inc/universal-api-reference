# Find One Record with NileDesk

Finds one record in NileDesk by filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/FindOneRecord`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Find One Record](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[]` | body | `array<string>` | no | Optional list of field keys to return. Leave empty to return all fields. |
| `filters` | body | `object` | no | Optional NileDesk filter object, for example {"logic":"and","rules":[{"field1":"value","operator":"eq"}]}. |
| `process_id` | body | `string` | no | Optional process or board item identifier to narrow the search. |
| `template_id` | body | `string` | yes | The NileDesk template to query. |
