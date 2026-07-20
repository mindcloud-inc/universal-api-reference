# List Form Step Answers with Florm

Retrieves answers for a Florm form step.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/answers/form/:form_guid/step/:step_id`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [List Form Step Answers](https://api.florm.io/docs#/default/form_answers_step_v1_answers_form__form_guid__step__step_id__get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_guid` | path | `string` | yes | GUID of the Florm form. |
| `step_id` | path | `number` | yes | Numeric Florm step identifier. |
| `skip` | query | `number` | no | Number of answer records to skip. |
| `limit` | query | `number` | no | Maximum number of answer records to return. |
| `is_completed` | query | `boolean` | no | Filter answers by completion state. |
