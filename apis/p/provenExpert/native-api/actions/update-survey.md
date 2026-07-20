# Update Survey with ProvenExpert

Updates an existing survey in ProvenExpert.

## Endpoint

- **Method:** `POST`
- **Path:** `/survey/update`
- **Base URL:** `https://www.provenexpert.com/api/v1`
- **Official documentation:** [Update Survey](https://developer.provenexpert.com/index_en.html#survey-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter.code` | body | `string` | yes | Survey code of the survey to update. |
| `data.active` | body | `number` | no | Whether the survey should be active after the update. |
