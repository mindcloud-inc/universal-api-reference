# List Fields with EventGeek

Retrieves custom field records from EventGeek.

## Endpoint

- **Method:** `GET`
- **Path:** `/fields`
- **Base URL:** `https://app.circa.co/api/v1`
- **Official documentation:** [List Fields](https://docs.circa.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields_for` | body | `string` | yes | Object type to list fields for: Event, Company, or Contact. |
