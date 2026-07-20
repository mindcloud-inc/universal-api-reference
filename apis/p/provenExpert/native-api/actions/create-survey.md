# Create Survey with ProvenExpert

Creates a survey in ProvenExpert.

## Endpoint

- **Method:** `POST`
- **Path:** `/survey/create`
- **Base URL:** `https://www.provenexpert.com/api/v1`
- **Official documentation:** [Create Survey](https://developer.provenexpert.com/index_en.html#survey-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.name` | body | `string` | yes | Name of the survey to create. |
| `data.pos` | body | `number` | no | Whether the survey should be created as a point-of-sale survey. |
