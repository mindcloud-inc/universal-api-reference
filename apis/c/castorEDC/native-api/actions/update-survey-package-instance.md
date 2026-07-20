# Update Survey Package Instance with Castor EDC

Updates a survey package instance in Castor EDC.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/study/:study_id/survey-package-instance/:survey_package_instance_id`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Update Survey Package Instance](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `survey_package_instance_id` | path | `string` | yes | The survey package instance UUID. |
| `locked` | body | `boolean` | no | Lock or unlock the survey package instance. |
| `sent_on` | body | `string` | no | UTC datetime when the survey package instance was sent. |
