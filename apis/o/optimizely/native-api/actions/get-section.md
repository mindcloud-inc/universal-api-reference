# Get Section with Optimizely

Retrieves a section from an Optimizely experiment.

## Endpoint

- **Method:** `GET`
- **Path:** `/experiments/{experimentId}/sections/{sectionId}`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [Get Section](https://docs.developers.optimizely.com/web-experimentation/reference/get_section)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experiment_id` | path | `string` | yes | The multivariate experiment id. |
| `section_id` | path | `string` | yes | The section id. |
