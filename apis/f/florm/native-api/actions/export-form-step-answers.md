# Export Form Step Answers with Florm

Creates an export task for Florm form step answers.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/export/form/step`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [Export Form Step Answers](https://api.florm.io/docs#/default/export_answers_step_form_v1_export_form_step_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Export file type. |
| `step_id` | body | `number` | yes | Numeric Florm step identifier. |
| `form_guid` | body | `string` | yes | GUID of the Florm form to export answers for. |
