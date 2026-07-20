# List Form Answers with Florm

Retrieves answers for a Florm form.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/answers/form/:form_guid`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [List Form Answers](https://api.florm.io/docs#/default/form_answers_v1_answers_form__form_guid__get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_guid` | path | `string` | yes | GUID of the Florm form. |
| `skip` | query | `number` | no | Number of answers to skip. |
| `limit` | query | `number` | no | Maximum number of answers to return. |
| `search_query` | query | `string` | no | Search text applied to Florm answers. |
| `is_completed` | query | `boolean` | no | Filter answers by completion state. |
