# Find Many Records with NileDesk

Finds multiple records in NileDesk by filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/FindManyRecord`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Find Many Records](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[]` | body | `array<string>` | no | Optional list of field keys to return. Leave empty to return all fields. |
| `filters` | body | `object` | no | Optional NileDesk filter object, for example {"logic":"and","rules":[{"field1":"value","operator":"eq"}]}. |
| `limit` | body | `number` | no | Optional maximum number of records to return. |
| `process_id` | body | `string` | no | Optional process or board item identifier to narrow the search. |
| `sort` | body | `object` | no | Optional NileDesk sort object, for example {"field":"_id","sort_by":"desc"}. |
| `template_id` | body | `string` | yes | The NileDesk template to query. |
